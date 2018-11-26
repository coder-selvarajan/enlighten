# Basics

Install Visual Studio Code and add following extentions

- Brackets pair
- Live server
- ES6 Code snippets

To find the time it took to execute the scripts:

```js
	console.time('Hello')
	console.log('hello world')
	console.log('hello world')
	console.log('hello world')
	console.log('hello world')
	console.timeEnd('Hello')

	RESULT:
	==>   Hello:
			0.05898324 sec
```

## Declaration: Var, Let, Const 

* Var : variable declaration
* Let : Similar to Var
* Const: cannot reassign, but object's property can be changed. 

```Javascript
	const msg = "Hello world";
	Msg = "Welcome";  // not accepted
	
	const person = { name: "ABC", age: 30 };
	Person.age = 35;   // accepted

	Const num = [1,2,3,4,5];
	Num.push(6);   // accepted
```

### Primitive datatypes:

	1. String
	2. Number
	3. Boolean
	4. Null
	5. Undefined
	6. Symbols (ES6)

### Reference data types:

	1. Array literals
	2. Object literals
	3. Functions
	4. Dates
	5. Anything else..


### Dynamically typed language

- The same variable can hold multiple types
- We don’t need to specify types
- Typescript - superset of JS - allow static typing

To find type of a variable use: 

    console.log(typeof age);

---

## Conversion

**To String 1:**
```Javascript
	let a;
	a=String(5);
	a=String(4+6);
	a=String(true);
	a=String(new Date());
	a=String([1,2,3,4]);
```

**To String 2:**
```Javascript
	let a;
	a=(5).toString();
	a=(true).toString();
```

**To Number:**
```Javascript
	a = Number('5')
	a.toFixed(2); // 5.00

	b = Number(true);   //1
	b = Number(false);  //0
	b = Number(null);    //0
	b = Number('hello');      //NaN
	b = Number([1,2,3,4]);  //NaN

	b = parseInt('100');          //100
	b = parseFloat('100.30');  //100.30
```

## Math Operations
```Javascript
	Math.PI
	Math.E
	Math.round(2.4); //2
	Math.ceil(2.4); //3
	Math.floor(2.8);  //2
	Math.sqrt(64);  //8
	Math.abs(-3);  //3
	Math.pow(8,2);  //64
	Math.min(3,7,2,5,6); //2
	Math.random();
	Math.floor(Math.random() * 20);
```
---

## String methods 

* concat
* toUpperCase
* toLowerCase
* length
* concat
* firstName[2];
* firstName.indexOf('l');
* lastIndexOf('l');
* charAt('2');
* firstName.charAt(firstName.length - 1);
* substring(0, 3);
* slice(0,3)
* slice(-3);
* split(' ');
* replace()
* includes('hello') //whether word exist or not

---

## Template strings 

### ES5:

```html
	Html = '<ul> ' +
			'<li>Name: ' + name + '</li>' + 
			'<li>Age: ' + age + '</li>' + 
			'<li>Job: ' + job + '</li>' +
			'<li>City: ' + city + '</li>' +
	'</ul>';
```

### ES6:

```html
	Html = `<ul> 
			<li>Name: ${name} </li> 
			<li>Age: ${age} </li>
			<li>Job: ${job} </li>
			<li>City: ${city} </li>
			<li>City: ${4+6} </li>
			<li>City: ${ fnDisplay() } </li>
			<li>City: ${age>30 ? 'over 30' : 'under 30' } </li>
			</ul>`;
```
---

## Arrays

```Javascript
	const num = [1,2,4,6,8,3];
	const num2 = new Array(23,5,6,34,75);
	var mix = [22,'apple', true, undefined, null, {a:1, b:2}, new Date()];
```

## Functions

* push();
* indexOf()
* isArray()
* unshift()
* Pop()
* Shift()
* Splice(1,3)
* Reverse()
* Concat()
* Sort()
* Sort( function(x,y) { return x-y; } );
* Find ( function(num) { return num < 50; } } 

---

## Objects

```Javascript
	const person = { 
		firstName: 'Senthamilan',
		lastName: 'Semmai',
		age: 40,
		hobbies: ['nature', 'social'],
		address: {
			City: 'thanjavore',
			State: 'TN'
			},
		getBirthyear: function(){
			return 1978;
			}
		};

	Person.firstName;  //Result: Senthamilan
```

**Date**

```Javascript
	var d = new Date();
```

## Conditions
	 
```Javascript
	// Equel to (== vs ===):
	If (n == 100) // checks the value only.
	If (n === 150)  //checks the type & value
```

```Javascript
	//var id;
	if(typeof id == 'undefined'){
		console.log('msg: id undefined');
	}
```

