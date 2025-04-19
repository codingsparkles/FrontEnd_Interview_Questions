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

157.

```javascript 
function fetchData() {
  return new Promise((resolve) => {
    setTimeout(() => {
      resolve("Data fetched!");
    }, 0);
  });
}
console.log(result);
fetchData().then((result) => {
  console.log(result);
});
```

157.

```javascript 

const fruit = {
  name: 'apple',
  calories: 95
};
Object.seal(fruit);
delete fruit.calories;
console.log(fruit.calories);
```


157.

```javascript 
console.log(Object.is(+0), Object.is(-0))
```

158.

```javascript 
const property = 'firstName';
const id = 1001;
const person = {
  id,
  [property]: 'James'
};
console.log(Object.keys(person)); // [id, firstName]
```

159.

```javascript 
function print() {
  return function() {
    return "Hello, Coder!";
  }
}      
const result = print();
console.log(result());
```

160.

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

for(key in user.address){
  console.log(key); // street, city, country
}
```

161.

```javascript 
const nestedArray = [1, [2, [3, 4], 5], 6];
const flattenedArray = nestedArray.flat(1);
console.log(flattenedArray); // [ 1, 2, [ 3, 4 ], 5, 6 ]
```

162.

```javascript 
function Person(name) {
  this.name = name;
  this.sayName = function() {
      console.log(`My name is ${this.name}`);
  }.bind(this);
}

const bob = new Person('John');
bob.sayName(); // Output: My name is John
```

163.

```javascript 

function add(a, b, c) {
  return a + b + c;
}

const addFive = add.bind(null, 5);
console.log(addFive(10, 15)); // Output: 30
```

164.

```javascript 
function multiply(factor) {
  return this.value * factor;
}

const context = { value: 10 };
const multiplyByTwo = multiply.apply.bind(multiply, context, 2);
console.log(multiplyByTwo()); // Output: 20
```

165.

```javascript 
function greet(greeting, punctuation) {
  return `${greeting}, ${this.name}${punctuation}`;
}

const person = { name: 'Alice' };
const result1 = greet.apply(person, ['Hello', '!']);
console.log(result1); // Output: Hello, Alice!
```

166.

```javascript 
const person = {
  name: 'Code',
  a: function() {
    return this.name
  },
  b() {
    return this.name
  },
  c: () => {
    return this.name
  },
}
console.log(person.a(), person.b(), person.c()); // Code Code undefined
```

167.

```javascript 
const compose = (a, b) => (x) => a(b(x));

const a = (num) => num * 2;
const b = (num) => num - 1;

const c = compose(a, b);

console.log(c(20)); // 38
```

168.

```javascript 
let a = 10;
const b = --a;
const c = a++;
console.log(a, b, c);  // 10 9 9
```

169.

```javascript 
console.log(Boolean('false'), Number('number'), Number(null), Number(false))  // output: true NaN 0 0
```


170.

```javascript 
(async () => {  
  await Promise.all([1,2,Promise.resolve(3), Promise.resolve(4)]).then((value) => {
    console.log(value)
  }, (error) => {
    console.log(error)
  })
})() // Output: [ 1, 2, 3, 4 ]
```

171.

```javascript 
console.log([[[[10]]]] + 1, [[[[10]]]] - 1) // Output 101 9
```

172.

```javascript 
(async () => {  
  await Promise.all([1,2,Promise.reject('Error'), Promise.resolve(4)]).then((value) => {
    console.log(value)
  }, (error) => {
    console.log(error)
  })
})() // Output: Error
```

173.

```javascript 
for (var i = 0; i < 5; i++) {
  setTimeout(() => console.log(i), 0)
}

for (let i = 0; i < 5; i++) {
  setTimeout(() => console.log(i), 0)
}
```

174.

```javascript 
const arrayOfObjects = [{ a: 1 }, { b: 2 }, [{ c: 3 }, { d: 4 }]];
const flattenedObjects = arrayOfObjects.flat();
console.log(flattenedObjects); // Output: [{ a: 1 }, { b: 2 }, { c: 3 }, { d: 4 }]
```

175.

```javascript 
const filePath = String.raw`C:\Development\profile\aboutme.html`;
console.log(`File Path: ${filePath}`);
```

176.

```javascript 
let a = 1;
const promise = new Promise((resolve) => {
  console.log(a++);
  resolve();
  console.log(++a);
});

promise.then(() => {
  console.log(a++);
});
```

177.

```javascript 
console.log(++a);
console.log(a++);
```


178.

```javascript 
console.log([...'coding', ...'sparkles'].join(''))
```

179.

```javascript 
console.log(`${(a => a)('I love')} coding!`);
```

180.

```javascript 
const fruits = ["Banana", "Orange", "Apple"]

if (fruits.includes('Mango')) {
  console.log('Will purchase it!');
} else {
  console.log(`We don't purchase it!`);
}
```

181.

```javascript 
const myValue = 21;

function getValue() {
  console.log(typeof myValue);
  myValue = 'CodingSparkles!';
}

getValue();
```

182.

```javascript 
const myPromise = Promise.reject('Fetching Data Failed!');

(async () => {
  try {
    console.log(await myPromise);
  } catch {
    console.log(`Oops didn't work`);
  } finally {
    console.log('Oh finally!');
  }
})();

console.log(Number('2') === +'2' === 2);
```

183.

```javascript 
const [a, b= 10] = [5, , 15, 20, 25, 30];
console.log(a+b);
```

184.

```javascript 
function addToList(item, list) {
  list.push(item);
  return list;
}

const result = addToList('apple', ['banana']);
console.log(result);
```

185.

```javascript 
const set = [...new Set([1, 2, 3, 4, 5])];
set.splice(1, 1, '2');
console.log(set.includes('2'));
```

186.

```javascript 
const obj = { 1: 'a', 2: 'b', 3: 'c' };
console.log(obj.hasOwnProperty(2));
```

187.

```javascript 
for (let i = 1; i < 4; i++) {
  if (i === 3) break;
  console.log(i);
}
```

188.

```javascript 
String.prototype.testMessage = () => {
  return 'Hello, Coder!';
};
const message = 'Hi';
console.log(message, message.testMessage());
```

189.

```javascript 
console.log(typeof typeof +'10');
```

190.

```javascript
const box = { x: 10, y: 20 };

Object.freeze(box);

const shape = { ...box};
shape.x = 100;

console.log(shape);
```

191.

```javascript
console.log([10]+[20]+[30]) 
```

192.

```javascript
const userData = [{
  "id": 1,
  "first_name": "Marlo",
  "last_name": "Menel",
  "email": "mmenel0@msu.edu",
  "gender": "Male"
}, {
  "id": 2,
  "first_name": "Laughton",
  "last_name": "Rowantree",
  "email": "lrowantree1@ed.gov",
  "gender": "Male"
}, {
  "id": 3,
  "first_name": "Aurilia",
  "last_name": "McGowan",
  "email": "amcgowan2@ed.com",
  "gender": "Female"
}];

console.log(userData.filter(item => item.email.includes('@ed')).map(item => item.id));
```

193.

```javascript
function nums(a, b) {
  if (!(a && b)) {
    return console.log('a or b or both values are empty');
  }  
  if (a === b) {
    return console.log('Both are equal');
  }
  if (a > b) {
    return console.log('a is bigger');
  }
  console.log('b is bigger');
}
nums(5, 4);
nums(1);
nums(6, 6);
```

194.

```javascript
const name = 'Coding';
console.log(name()); // TypeError
```

195.

```javascript
const colorConfig = {
  red: !0,
  blue: false,
  green: !!'',
  black: 1,
  yellow: 0,
};

const colors = ['pink', 'red', 'blue'];

console.log(colors.map(item => !colorConfig[item]));  // [ true, false, true ]
```

197.

```javascript
const newMap = new Map();
const newFunc = () => 'sparkles';
newMap.set(newFunc, 'Hi Coders!');
newMap.get('sparkles');
console.log(newMap.get(newFunc));  // Hi Coders!
```

198.

```javascript
const [x, ...y] = [1, 2, 3, 4, 5];
const [a, , , b] = y;
console.log(x+a+b); // 8
```

199.

```javascript
console.log(Math.min(1,2,0), Math.max([10,20,6]))  // Infinity -Infinity 0 20
```

200.

```javascript
console.log(Math.round(-0.5) === 0) // true
```

201.

```javascript
(() => {
  if (!fn) {
    function fn() {
      console.log("2");
    }
  }
  fn();
})()  // 2
```

202.

```javascript
const obj = {
  foo: 'bar'
}
const obj2 = { ...obj }
console.log(['foo'] in obj === 'foo' in obj)  // true
```

203.

```javascript
function log(a,b,c,d) {
  console.log(a,b,c,d)
  arguments[0] = 'coding'
  arguments[3] = 'sparkles'
  console.log(a,b,c,d)
}

log(10,20,30); // 10 20 30 undefined 'coding' 20 30 undefined
```

204.

```javascript
function countVowels(str) { 
  return [...str].reduce((acc, item) => {
    return ['a', 'e', 'i', 'o', 'u'].includes(item.toLowerCase()) ? acc++ : acc;
  },0);
}

console.log(countVowels("Hello World")); // 0
```

205.

```javascript
console.log(1 + + '1' + + '1') //3
```

206.

```javascript
console.log(Object.is(0, Math.round(0.5)), Object.is(0, Math.round(-0.5))) // false false
```

207.

```javascript
const arr = [1,2].concat([3, 4]);
arr.push(7,8);
arr.unshift(5,6);
arr.splice(1,3);
console.log(arr); // [ 5, 3, 4, 7, 8 ]
```

208.

```javascript
const arr = [1,,2,,5];
console.log([...arr]); // [ 1, undefined, 2, undefined, 5 ]
console.log(arr.map(i => i * 2));  // [2, empty, 4, empty, 10]
```

209.

```javascript
async function a() {
  try {
    return await Promise.reject(1)
  } catch (e) {
    console.log(e)
  }
}

async function b() {
  try {
    return Promise.resolve(2)
  } catch (e) {
    console.log(e)
  }
}

b();
a(); // 1
```

210.

```javascript
const a = [1,2,3];
const b = a.unshift(0);
console.log(a.length, b); // 4 4
```

211.

```javascript
if(true) {
  function test() {
    console.log("Coding")
  }
}
test();
function test() {
  console.log("Sparkles");
}
test(); // Coding Coding
```

212.

```javascript
console.log(...new Set([
  ...Object.keys({a: 1, b: 2}),
  ...Object.keys({b: 2, a: 1})
])); // a b
```

213.

```javascript
let count = 1;
function a() {
  console.log(count++)
  return {
    a: function() {
      console.log(count)
      return a()
    }
  }
}

a().a() // 1 2 2
```

214.

```javascript
console.log('1' + !undefined, 1 + !undefined); // 1true 2
```

215.

```javascript
const str = "Coder";
str[3] = "i";
console.log(str); // Coder
```

216.

```javascript
const a = [1,2,3]
b = [...a, 4]
b.push(5)
console.log(b[3]) // 4
```

217.

```javascript
console.log(('b' + 'a' + + 'b' + 'a').toLowerCase()) // banana
```

218.

```javascript
const a = (1,2,3)
console.log(a) // 3
```

219.

```javascript
let num

for (let i = 0; i < 5; i++) {
  num = i++
  setTimeout(() => {
    console.log(num)
  }, 0)
} // 4 4 4
```

220.

```javascript
function greet(name, callback) {
  console.log(`${name}`);
  callback();
}
function getMessage() {
  console.log("Happy Coding!");
}
greet("Hello", getMessage); // Hello, Happy Coding!
```

221.

```javascript
function detectType(data) {
  return typeof data;
}

console.log(detectType(null) == detectType([]),  detectType(new Object()) == detectType(new Set())) // true true
```

222.

```javascript
function checkStatus(isSuccess) {
  if (isSuccess) {
    const message = "You are successful.";
  } else {
    const message = "You failed, try again!";
  }

  return message;
}

console.log(checkStatus(!'')); // Reference Error
```

223.

```javascript
console.log(`${'Welcome'[0]+'Coder'[1]+'World'[0]}`); // Yet to  ->
```

224.

```javascript
console.log("Start");
setTimeout(() => {
 console.log("Timeout");
}, 0);
Promise.resolve().then(() => {
 console.log("Promise");
});
console.log("End"); // Done
```

225.

```javascript
const add = x => y => z => {
  return x + y * z;
};

console.log(add(3)(8)(2)); // 19
```

226.

```javascript
const printValues = ({ x, y, z = 5 }) => {
  console.log(x, y, z);
};

printValues({x: 10, y: 20}); // 10 20 5
```

227.

```javascript
const printArrValues = ([a, b]) => {
  [b, a] = [a, b];
  console.log(a*2,b*5);
};

printArrValues([5, 10]); // 20 25
```

228.

```javascript
function sumMatrixDiagonal(matrix) {
  return matrix.reduce((acc, item, index) => acc+item[index], 0);
}
console.log(sumMatrixDiagonal([[1, 2, 3], [4, 5, 6], [7, 8, 9]]));
```

229.

```javascript
function findSmallest(arr) {
  return Math.min(arr);
}

console.log(findSmallest([30, 40, 50, 10, 20]));
```