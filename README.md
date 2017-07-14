### How delete operator works?

```
The delete operator is used to delete the property of an object.
```

The example for delete operator is given below.

```javascript
var abc = { x: 10 };
var result = (function () {
    delete abc.x;
    return abc.x;
})();

alert(result);
```

Lets take a minute and guess the output !!

> Yes you are correct, It will return undefined.

Ok lets try the same delete with another example

```javascript
var abc = 10;
var result = (function () {
    delete abc;
    return abc;
})();

alert(result);
```

Now guess what will be the output?

>If you say 'undefined' no you are wrong. The output is 10. But why ????

As i mentioned earlier it is used the delete the object property only. ```delete``` operators don’t affect local variables.

Ok lets try the same delete with another example

```javascript
var Employee = {
  company: 'xyz'
}
var emp1 = Object.create(Employee);
delete emp1.company
console.log(emp1.company);
```

The output would be ```xyz```. Here, ```emp1``` object has ```company``` as it is prototype property. The ```delete``` operator doesn’t delete prototype property.

```emp1``` object doesn’t have company as its own property.

Please find the output for the below object.
```javascript
console.log(emp1);
console.log(Employee);
```

![image](https://user-images.githubusercontent.com/6780840/28212263-3d8014be-68be-11e7-93cb-0aeb8f4fde89.png)

However, we can delete the ```company``` property directly from the ```Employee``` object using ```delete Employee.company```.
