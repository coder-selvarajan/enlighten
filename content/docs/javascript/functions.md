## Functions

### Function expressions

```javascript
    const square = function(x) {
        return x * x;
    };
    const square = function(x = 4) {
        return x * x;
    };
    console.log(square(11)); // Result: 121
```

#### Immediately invokable function expressions

```javascript
    (function(name) {
        Console.log("Hello " + name);
    })("Brad");

    // Result: Hello Brad
```

### Property methods

```javascript
    const todo = {
        add: function(){
            console.log('Adding todo…');
        }
        edit: function(id){
            console.log('Editing - ' + id);
        }
    }

    todo.delete = function(){
        console.log('deleting todo..');
    }

    todo.add();
    todo.edit(2);
    todo.delete();
```
---

### FOR EACH

#### Type 1:

```javascript
    const cars = ["Ford", "Chevy", "Honda", "Toyota"];

    cars.forEach(function(car) {
        console.log(car);
    });

    // Result:
    Ford;
    Chevy;
    Honda;
    Toyota;
```

#### Type 2:

```javascript
    const cars = ['Ford','Chevy','Honda','Toyota'];
    cars.forEach(function(car, index){
        console.log(`${index} : ${car}`);
    });

    // Result:
    0 : Ford
    1 : Chevy
    2 : Honda
    3 : Toyota
```

#### Type 3:

```javascript
    const cars = ["Ford", "Chevy", "Honda", "Toyota"];
    cars.forEach(function(car, index, array) {
        console.log(`${index} : ${car}`);
        Console.log(array); //prints the entire array for each iteration
    });
```
---

### MAP - ForEach 

```javascript
    const users = [
        {id:1, name:'John'},
        {id:2, name:'Kense'},
        {id:3, name:'Saril'}];
        
    const ids = users.map(function(user){
        return user.id;
    });

    console.log(ids);  // Result:  (3): [1,2,3] 
```

### For IN loop

```javascript
    const user = {
        firstName: 'John',
        lastName: 'Shen',
        Age: 40
    }

    for(let x in user){
        console.log(` ${x} : ${user[x]} `);
    }

	// Result: 
	firstName : John
	lastName : Shen
	Age : 40
```