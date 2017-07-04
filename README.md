### How delete operator works?

```
The delete operator is used to delete the property of an object.
```

> How to create function overloading in JavaScript?

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
