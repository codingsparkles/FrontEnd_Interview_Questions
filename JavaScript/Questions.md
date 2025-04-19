1.

```javascript
const arr = [5, 10, 15];
arr[20] = 20;
console.log(arr[19])
console.log(arr.length)
```

2.

```javascript
const calculate = {
  a : 10,
  increment(){
    this.a++;
  },

  decrement() {
    this.a--;
  },

  result() { console.log(this.a) }
}

calculate.increment();
calculate.decrement();
calculate.increment();
calculate.result();
```

3.

```javascript
const vehicle = {
  color: 'yellow',
  result() {
    console.log(vehicle.name);
  }
}

console.log(vehicle.result());
```

4.

```javascript
const details = [
  { id: 1, count : 10, required: true},
  { id: 2, count : 15, required: false},
  { id: 3, count : 20, required: false},
  { id: 4, count : 25, required: true}
]

const filteredItems= details.filter(detail => detail.required).map(item => item.id);
console.log(filteredItems);

console.log(undefined ?? null ?? false)
```

5. 

```javascript
const arr = [1, 2, 3];
let nums = arr.join('');
console.log(nums++);
console.log(++nums);
```

6.

```javascript
function multiply(a){
  return function(b){
    return function(c){
      return a*b*c;
    }
  }
}

const multiply1 = multiply(5);
const multiply2 = multiply1(7);
const result = multiply2(2);
console.log(result);

console.log(multiply(1)(2)(3))
```

7.

```javascript
const arr = ['Apple', 'Mango', 'Grapes'];
const arr1 = [arr[0],...['Lemon', 'Orange']];
console.log(arr1);
```

8.

```javascript
const str = "Sparkles";

console.log(str.at(-2) === str.substr(str.length -2, 1))
```

9.

```javascript
const name = 'Madam';
console.log(`${name.at(-1).toUpperCase()}${name.substr(1,4)}`);
```

10.

```javascript
const str = 'sparkles';
console.log(str.charAt[8])
console.log(str[8])
console.log(str[8] === str.charAt(8))
console.log(undefined === undefined)
```

11.

```javascript
console.log(`${'c'.padEnd(3, 'x')}ing`)
```

12.

```javascript
const message = "       Hello Folks!       ";
const text = message.trim();
console.log(message.trim());
```
13.

```javascript
const message = "Hello Folks!";
console.log(message.at(-2) , message.indexOf(-2))
```

14.

```javascript
const message = `I love coding, Coding is fun`;
console.log(message.replaceAll('coding', 'development'))
```

15.

```javascript
function foo() {
  console.log(bar);
  var bar = 2;
}

foo();
```

16.

```javascript
const fruit = 'apple';
console.log(`${fruit} is healthy`);
```

17.

```javascript
console.log([1, 2, 3, 4, 5].toSpliced(1,2))
```

18.

```javascript
const calc = function() {
  let count = 0;
  return function() {
    console.log(count++)
  }
}
const a = new calc();
a();
a();
a();
```

19.

```javascript
const obj = { id: 10, name: "Sparkle", age: 30 };
const { id: userId, name } = obj;
console.log(userId, name);
```

20.

```javascript
const employee = {
  name: 'John Deo',
  id: 1,
  performance: {
    score: 100
  }
}

console.log(employee?.performance?.score, employee?.performance?.rank);
```

21.

```javascript
const arr = [[1, 2, 3, 4, 5].pop()];
arr.unshift(3,4);
console.log(arr)
```


22.

```javascript
const arr = ["fun", "coding", "love", "I"];
console.log(arr.every(item => item.includes['o']))
console.log(arr.sort((a,b) => a.length - b.length));
```

23.

```javascript
const employee = {
  name: 'John Deo',
  id: 1,
  performance: {
    score: 100
  }
}
console.log(!!employee?.performance?.rank ?? "Not Set", !!employee?.performance?.rank || "Not Set")

console.log(employee?.name && employee?.performance?.score);
console.log(employee?.performance?.rank ?? 0);
```

24.

```javascript

const details = [
  { id: 1, count : 10, required: true},
  { id: 2, count : 15, required: false},
  { id: 3, count : 20, required: false},
  { id: 4, count : 25, required: true}
]

const filteredIds = details.filter(detail => detail.count > 15).map(item => item.id);
console.log(filteredIds);
```

25.

```javascript

const name="Jaquar", id = 1000;
const car ={ name, id};
console.log(car);

```

26.

```javascript
const arr = ["fun", "coding", "love", "I"];
console.log(arr.filter(item => item.length >= 4));
```

27.

```javascript
const obj1 = { name: 'Audi', id: 1000 };
const obj2 = { name: 'Jaquar', id: 1001 };
console.log({...obj1, ...obj2});
```

28.

```javascript
const message = `I love coding, Coding is fun`;
console.log(message.search("Coding"))
```

30.

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.toReversed();
console.log(fruits);
```

31.

```javascript
const { a, b = 10 } = { a: 30 };
console.log(a+b);
```

32.

```javascript
const arr = [[1, 2, 3, 4, 5].pop()];
arr.unshift(3, 4);
console.log(arr);
```

33.

```javascript
const arr = ["fun", "coding", "love", "I"];
console.log(arr.sort((a, b) => a.length - b.length));
```

34.

```javascript
const obj1 = { name: "Audi", id: 1000 };
const obj2 = { name: "Jaquar", id: 1001 };
console.log({ ...obj1, ...obj2 });
```

35.

```javascript
const message = `I love coding, Coding is fun`;
console.log(message.search("Coding"));
```

36.

```javascript
const arr = ["Apple", "Mango", "Grapes"];
console.log(arr.reverse((a, b) => a - b));
```

37.

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.reverse();
console.log(fruits);
```

38.

```javascript
const numbers = [1, 2, 3];
numbers[10] = 10;
console.log(numbers);
```

39.

```javascript
console.log([...[1, 2, 3, 4], 5].unshift(0));
```

40.

```javascript
const add = async (a, b) => {
  const result = a + b;
  console.log(result);
};
```

41.

```javascript
const insert = (arr1, item, arr2) => {
  return [...new Set([...arr1, item, ...arr2])];
};

console.log(insert([1, 2, 3, 4], 5, [1, 2, 3, 4]));

console.log(insert([1, 2, 3, 4], 6));
```

42.

```javascript
const arr = [1, 2, 3, 4];
arr.shift();
console.log(arr);
```

43.

```javascript
const arr = [["a", "b"], "c", ["d", "e"]];
console.log(arr.flat());
```

44.

```javascript
const arr = ["fun", "coding", "love", "I"];
console.log(arr.at(-2));
```

45.

```javascript
const { a, b = 2 } = { a: 10 };
console.log(a * b);
```

46.

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
console.log(
  fruits.reduce(
    (str, item) => (item.length > 5 ? [...str, item].toString() : item),
    ""
  )
);
console.log(
  fruits.reduce(
    (str, item) => (item.length > 5 ? console.log(item, str) : item),
    []
  )
);
```

47.

```javascript
const fruits = ["Banana", "Pineapple", "Apple", "Jackfruit"];
console.log(fruits.filter((item) => item.length > 5));
console.log(fruits.sort((a, b) => a.length - b.length));
console.log(
  fruits.reduce((arr, item) => {
    return item.length > 5 ? [...arr, item] : [item];
  }, [])
);
```

48.

```javascript
const str = "madam";
const strArr = [...str];
const newArr = strArr.reduce((a, i) => [...a, i], []);
console.log(newArr);
console.log([].unshift("m"));
```

49.

```javascript
const fruits = ["Banana", "Pineapple", "Apple", "Jackfruit"];
console.log(fruits[fruits.indexOf("Apple")] === fruits.at(-2));
console.log(fruits.at(2) === fruits.at(-2));
```

50.

```javascript
console.log([1, 2, 3, 4].at(3));
```

51.

```javascript
console.log([...new Set(["a", "b", "a", "c", "d", "b"])]);
```

52.

```javascript
const fruits = ["Banana", "Pineapple", "Apple", "Jackfruit"];
console.log(fruits.findIndex((item) => !item.includes("r")));
console.log(fruits.findIndex("Apple"));
```

53.

```javascript
const employee = [
  {
    id: "1",
    firstName: "Tom",
    lastName: "Cruise",
  },
  {
    id: "2",
    firstName: "Maria",
    lastName: "Sharapova",
  },
  {
    id: "3",
    firstName: "James",
    lastName: "Bond",
  },
];
console.log(
  employee?.map(({ firstName, lastName }) => `${firstName} ${lastName}`)
);

console.log(employee?.find((item) => item.id == 2)?.firstName);
```

54.

```javascript
const nums = [1, 2, 3, 4, 5];
nums.length = 2;
nums.length = 4;
console.log(nums);
```

55.

```javascript
const fruit = {
  name: "apple",
  color: "red",
};
fruit["calories"] = 95;
Object.seal(fruit);
fruit["price"] = 100;
console.log(fruit.calories, fruit.price);
```

56.

```javascript
const vehicle = {
  name: "Honda",
  color: "Grey",
};

Object.defineProperties(vehicle, {
  color: { value: "blue" },
  price: { value: "15l" },
});

console.log(vehicle.color, vehicle.price);
```

57.

```javascript
const person = {
  fullName: function () {
    return `${this.firstName} ${this.lastName}`;
  },
};
const person1 = {
  firstName: "John",
  lastName: "Deo",
};

console.log(person.fullName.call(person1));
```

58.

```javascript
const vehicle = {
  name: "Honda",
  color: "Grey",
};
Object.seal(vehicle);
Object.defineProperty(vehicle, "color", { value: "blue" });
console.log(vehicle.color);
```

59.

```javascript
function Person(name, age) {
  this.name = name;
  this.age = age ?? 21;
}
const object = new Person("John");
console.log(object);

console.log(["a", "b", "c"].concat(["b", "c", "d"]).sort());
```

60.

```javascript
function message(...args) {
  return console.log(
    `${this.name} is ${args[0]} ${args[1] ? `and ${args[1]}` : ""}`
  );
}
const person4 = { name: "John" };
message.apply(person4, ["awesome", "", "fantastic"]);
```

61.

```javascript
const arr = [5, 10, 15, 2, 25, 30];
arr.splice(3, 1, ...[20, 22, 23]);
console.log(arr);
```

62.

```javascript
const x = (y = [1, 2, 3, 4]);
x[2] = 30;
console.log(x, y);
```

63.

```javascript
const obj = { config: { title: "Page", action: "Run" } };
const {
  config: { title = "", action = "", status = "" },
} = obj || {};
console.log(title, action, status);
```

64.

```javascript
const arr = [1, 5, 7, 9, 11];
const [a, b, ...rest] = arr;
console.log(rest.reduce((total, item) => total + item, 0));
```

65.

```javascript
const arr = ["fun", "coding", "love", "I"];
console.log(arr.join("-").slice(9, 20));
```

66.

```javascript
const str = "Coder";
let a = str.split("");
a.splice(3, 2, ...["ing"]);
a = a.join("");
console.log(a);
```

67.

```javascript
console.log(
  ["a", "b", "a", "c", "d", "e"].findLastIndex((item) => item === "a")
);
```

68.

```javascript
const a = ["a", "b", "c", "d"];
const b = [...a];
a.toReversed();
b.reverse();
console.log(a, b);
```

69.

```javascript
console
  .log([3, 1, 6, 2, 4].find((item) => item < 3))
```

70.

```javascript
console.log(
  [1, "2", 3].map((num) => {
    if (isNaN(num)) return;
    return num * 2;
  })
);
```

71.

```javascript
const person = { id: 10, name: "John" };
const person1 = { ...person };
Object.freeze(person);
Object.seal(person1);
person.name = "Deo";
person1.name = "Deo";
console.log(person.name, person1.name);
```

72.

```javascript
let a = 10;
console.log(a);
setTimeout(() => {
  a++;
  console.log(a);
}, 0);
console.log(a);
```

73.

```javascript
const nums = [20, 15, 30, 35];
nums.unshift(5);
nums.push(10);
console.log(nums.sort());
```

74.

```javascript
const nums = [20, 15, 30, 35, -15];
console.log(Math.max(...nums));
console.log(Math.min(...nums));
```

75.

```javascript
const arr = [2, null, 1, "", undefined, 3];
console.log(arr.filter(Boolean));
```

76.

```javascript
console.log(!undefined + !null + false + "");
```

77.

```javascript
let a = 0;
setTimeout(() => console.log(++a));
Promise.resolve().then(() => console.log(a));
console.log(a);
```

78.

```javascript
let message = "Hello!";
console.log(message);
(function () {
  console.log(message);
  message = "World!";
})();
console.log(message);
```

79.

```javascript
const welcome = () => console.log("Hello!");
function welcome() {
  console.log("Hello!");
}
(function () {
  console.log("Hello!");
})();
```

80.

```javascript
const [a, b, , ...rest] = [1, 3, 5, 7, 9, 11];
const [c, d, ...rest1] = rest;
console.log(a, b, c, d);
```

81.

```javascript
function test(...args) {
  args.shift();
  console.log(...args);
}
test(1, 2, 3, 4, 5);
```

82.

```javascript
["a", "b", "c", "d"].forEach((item, index) => {
  if (index > 1) {
    return;
  }
  console.log(item);
});
```

83.

```javascript
function foo(x, y) {
  x = 0 in arguments ? x : 11;
  y = 1 in arguments ? y : 31;
  console.log(0 in arguments);
  console.log(1 in arguments);
}

foo(5, undefined);
```

84.

```javascript
function foo(x, y) {
  x = !!x ? x : 11;
  y = !!y ? y : 31;
  console.log(x + y);
}

foo(5, undefined);
console.log((undefined = !!undefined));
``` 

85.

```javascript
let w = 1,
  z = 2;
function foo(x = w + 1, y = x + 1, z = y + 1) {
  console.log(x, y, z);
}
foo();
```

86.

```javascript
const x = (y = z = 100);
console.log((x === y) === z);
```

87.

```javascript
let x = 100;
y = x;
x += 10;
y -= 5;
console.log(x, y);
```

88.

```javascript
const nums = [1, 2, 3, 4, 5];
let [a, b, c, ...rest] = nums;
[c, b] = [a, b, c];
console.log(a, b, c);
```

89.

```javascript
const arr1 = ["d", "a", "c"];
const arr2 = ["f", "b", "e"];
console.log([...arr1, ...arr2].sort());
console.log([...arr1, ...arr2]);
console.log(["d", "a", "c"].sort());
```

90.

```javascript
console.log([..."Orange"].reverse().reverse().join(''))
```

91.

```javascript
function func(x,y) {
  console.log(...arguments);
}
let x = 10, y = 20;
func(x++);
func(x++, y);
func(++x, y-1);
```

92.

```javascript
function findLength(a = [], b = []) {
  console.log(a.length, b.length);
}

findLength([1, 2]);
findLength([1, 2], [3, 4, 5]);
findLength([1, 2] + [3, 4, 5]);
```

93.

```javascript
const values = [1, [2, , 4], 5];
const [a, [b, c = 0, d], e] = values;
console.log(a, b, c, d, e);
```

94.

```javascript
function test(x, y) {
  console.log(0 in arguments);
  console.log(1 in arguments);
}

test(5);
test(10, 5);
```

95.

```javascript
console.log(typeof undefined, typeof NaN, typeof null)
```

96.

```javascript
function upper(str) {
  return str.toUpperCase();
}

console.log(`Hello, ${upper('Sparkles')} welcome!`)
```

97.

```javascript
function a(){
  b.apply(null, arguments);
}
function b(){
  console.log(arguments[0]);
}
a(10,20,30);
```

98.

```javascript
const a = Array.apply(null, { length: 4});
console.log(a);
```

99.

```javascript
const nums = [1, 5, 7];
console.log([...nums.keys()], [...nums.values()]);
```

100.

```javascript
const nums = Array.apply(null, { length: 4});
nums[1] = 10;
nums[3] = 20;
console.log(nums.map(item=> !!item));
```

101.

```javascript
const arr = [10, 20, 30];
arr.unshift(5);
arr.unshift();
console.log(arr[0]);
```

102.

```javascript
function foo(str) {
  console.log(str);
}
const name ="Coding";
const desc ="fun";
foo(`${name} is ${desc}!`);
```

103.

```javascript
const str = 'Coding'.split('');
str[0] ="c";
console.log(str.join(''));
```

104.

```javascript
const arr = [...new Set([1,2,1,3,2,4,5])];
console.log(arr[2]);
```

105.

```javascript
const nums = Array.apply(null, { length: 5});
nums[0] = 10;
nums[2] = 20;
nums[4] = 30;
console.log(nums.reduce((acc,item)=> acc + !!item , 0));
```

106.

```javascript
const a = [];
a[4] = 10;
console.log(a.length, a[2]);
```

107.

```javascript
const person = {
  name: 'coding',
  id: 100
};
const person1 = Object.assign({}, person);
person1.id = 101;
console.log(person);
```

108.

```javascript
const arr = [];
arr[0] = '';
arr[1] = 10;
arr[2] = 'a';
arr.forEach(item => console.log(!!item));

console.log(isNaN("a"), isNaN(false));
```

109.

```javascript
let name = {
  first: "coding",
  last: "sparkles",
};
delete name["last"];
function test() {
  console.log(name.first, name.last);  
}
test();
```

110.

```javascript
const arr = [];
arr[1] = 10;
arr[2] = '';
arr[4] = 20;
console.log(arr.filter(item => item));
```

111.

```javascript
function findMatching(arr1, arr2) {
  return arr1.filter(value => arr2.includes(value));
}

const array1 = [1, 2, 3, 4, 5];
const array2 = [4, 5, 6, 7, 8];
console.log(findMatching(array1, array2));
```

112.

```javascript
function extractSubstring(str, start, length) {
  return str.substr(start, length);
}
const msg = "Fantasy Coding!";
console.log(extractSubstring(msg, -12, 4));
```

112.

```javascript
const array = [1, 2, 3, 4, 5];
const nums = array
  .map((item) => item * 2)
  .filter((num, index, items) => items.includes(num/2));
console.log(nums);
```

113.

```javascript
const names = ['John'];
names.unshift('Smith');
const mergeNames = [...names, ...['Deo', 'William']];
console.log(mergeNames[2]);
```

114.

```javascript
console.log(a);
var a = 'Apple';
console.log(b);
let b = 'Orange';
```

115.

```javascript
const nums = [1, 3, 5, 7, 9, 11];
nums.length = 5;
console.log(nums[4], nums[5]);
```

115.

```javascript
let name = 'coding';
function test() {
  console.log(delete name, name);  
}
test();
```

116.

```javascript
function test() {
  console.log(x);
  x = 10 + '22';
  console.log(x);
  (function () {
    let x = 20;
    console.log(x++);
    return;
  }());
  console.log(x);
}

test();
```

117.

```javascript
const original = {
  name: "John",
  age: 30,
  address: {
      city: "New York",
      zip: "10001"
  }
};
const cloned = deepClone(original);
cloned.address.city = "Los Angeles";
console.log(original.address.city, cloned.address.city);
```

118.

```javascript
const user = {
  id: 1,
  name: 'John Doe',
  age: 30,
  address: {
      street: '123 Main St',
      city: 'Anytown',
      country: 'USA'
  }
};

const { name, age, address: { city, country } } = user;

console.log(`Name: ${name}, Age: ${age}, City: ${city}, Country: ${country}`);
```

119.

```javascript
const nums = [[0, 1], [2, 3], [4, 5]].reduce((accumulator, currentValue) => {
  return accumulator.concat(currentValue);
}, []);

console.log(nums);
```

120.

```javascript
let personPrototype = {
  greet: function() {
    console.log('Hello, ' + this.name);
  }
};

let john = Object.create(personPrototype);
john.name = 'John';
john.greet();
```

120.

```javascript
console.log(typeof foo);

function foo() {
  return "bar";
}
```

121.

```javascript
var foo = "bar";

let a = !'';
if (a) {
  function foo() {
    console.log("Hello");
  }
} else {
  function foo() {
    console.log("Coder");
  }
}

foo();
```

122.

```javascript
let count = 0;
(function() {
  if (count === 0) {
    let count = 1;
    console.log(count);
  }
  console.log(count);
})();
```

123.

```javascript
function test() {
  let a = b = [];
  a++;
  return a;
}
test();
console.log(typeof a, typeof b);
```

124.

```javascript
console.log(+true, +!!'1')
```

125.

```javascript
const shape = {
  radius: 10,
  diameter() {
    return this.radius *2
  },
  perimeter : () => 2 * Math.PI * this.radius,
}
console.log(shape.diameter());
console.log(shape.perimeter())
```

126.

```javascript
let a = 3;
let b = new Number(3).valueOf();
let c = 3;
console.log(a == b, a === b, b === c);
```

127.

```javascript
function test() {
  console.log("I am in testing!");
}
test.name = "Hello!"
console.log(test());
```

128.

```javascript
function getInfo(one, two, three) {
  console.log(one, two, three)
}

const person = "Adam";
const id = 1000;
getInfo`${person} with ${id} is selected.`
```

129.

```javascript
const getType = (...args) => {
  console.log(typeof args[0], typeof args[1]);
}
getType(100);
```

130.

```javascript
const getMathValue = (...args) => Math.ceil(args[args.length-2]);
console.log(getMathValue(5, '20.1234', 10))
```

131.

```javascript

const obj = {
  name: 'Adam',
  id: 100,
  name: 'Smith',
  id: 200
};
console.log(obj);
```

132.

```javascript

console.log(...new Set([[1,2], [3,5]].reduce((acc, cur) => acc.concat(cur), [5])));
```

133.

```javascript
const person = { id: 10, name: 'Adam'};
for(const item in person) { console.log(person[item])}
```

134.

```javascript

function profile(info, doj) {
  info.name = "Smith",
  doj = 1995
}
const info = { name: 'Maddy'};
const doj = 2000;
profile(info, doj);
console.log(info.name, doj);
```

135.

```javascript
const name = 'Coding';
const age = 25;
const person = { name, age};
console.log(Object.keys(person));
```

136.

```javascript
const arr = [['a', 'b'], [10], [1, 3, 5], [5, 15]];
console.log(...arr[[...arr[2]][0]]);
```

137.

```javascript
const nums = [1, 3, 5, 7, 9, 11];
const result = nums.forEach((item) =>  item * item);
console.log(result);
```

138.

```javascript
function func(a = 1, b = 2) {
  arguments[0] = 2;
  console.log(arguments[0] == b);
}
func();
```

139.

```javascript

const arr = [['a', 'b'], [2, 4, 6], ['c', 'd', 'e'], [3, 5]];
const result = arr.reduce((acc, item) => [...acc, ...item],[])?.filter(i => isNaN(i));
console.log(...result);
```

140.

```javascript
const arr = Array.from(Array(10).keys());
console.log(arr.reduce((acc, index) => !(index % 2) ? [...acc, index] : acc, []));
```

141.

```javascript
const albhaNumeric = ["a", 1, 2, "b", "c", 4];
delete albhaNumeric[4];
console.log(albhaNumeric[4], albhaNumeric.length);
```

142.

```javascript
const promise1 = Promise.resolve('One');
const promise2 = Promise.reject('Two');

Promise.all([promise1, promise2]).then(values => console.log([...values])).catch(reason => console.log(reason));
```

143.

```javascript
const nums = [1, 2, 3, 4, 5, 6, 7];
const result = nums.reduce((acc, item) => {
  if (!(item % 2)) {
    acc.unshift(item);
    return acc;
  }
  return acc;
}, []);
console.log(result);
```

144.

```javascript
const nums = [1, 3, , , 9, 11];
const result = nums.map((item) =>  ++item);
console.log(result);
```

145.

```javascript
var p = new Promise((resolve, reject) => {
  resolve(reject(Error('The Fails!')));  
})
p.then(msg => console.log(msg))
p.catch(error => console.log(error.message))
```

146.

```javascript
const a = [];
const b = [].length;
const c = a;
console.log(!!a && b || !!c); // (true && false || true)
```

147.

```javascript
function sum(a) {
  return function (b) {
    return function (c) {
      return a + b + c;
    };
  };
}
console.log(sum(true)(1)(false));
```

148.

```javascript
function test(a) {
  return function(b) {
    return !!a > b;
  };
}

let test1 = test(10);
console.log(test1(2));
```

149.

```javascript
const person = {
  name: 'test',
  age: 20,
  'account number': 1000,
}

console.log(person["age"], person["account number"]); // 20 1000
```


150.

```javascript
const arr1 = [1,2,3,4,5];
const arr2 = '1,2,3,4,5';
console.log(arr1 == arr2);
```

151.

```javascript
const arr = [2, 3, 4];
console.log(Math.pow(arr[0],2) === arr[2]);
```

152.

```javascript
const car = {
  name: 'Jaguar',
  owner: 'Tata Motors'
};
console.log(Object.seal(car)); // { name: 'Jaguar', owner: 'Tata Motors' }
```

153.

```javascript
const fruit = {
  name: 'apple',
  calories: 95
};
const cloned = {...fruit};
delete calories;
console.log(Object.hasOwn('calories')); // false
```

154.

```javascript
console.log(Object.is(null, undefined)) // false // ["true", "false", "null", "undefined"]
```

155.

```javascript

const fruit = {
  name: 'apple',
  calories: 95
};
fruit["price"] = 100;
Object.freeze(fruit);
delete fruit.price;
console.log(Object.values(fruit)); // [ 'apple', 95, 100 ]
```

156.

```javascript 
console.log(Object.hasOwn({a: 2}, 'a')); // true
```