js-debugging-talk
=================

Code snippeds for my "Debugging JS with Chrome" talk at FDC'14

##### console.log(), .warn(), .error(), .assert()
```javascript
var obj = {
  prop: 1, child: {
    prop: 2
    }
};
console.log(obj);
console.log('%O\n%o', document.body, document.body);
console.warn('something unexpected happened');
console.error('something went wrong');
console.assert("str" instanceof String, 'gotcha!');
```

##### console.count()
```javascript
document.addEventListener('keydown', function(event) {
  console.count(String.fromCharCode(event.keyCode));
});
```

##### console.time()
```javascript
function fibonacci(n) {
  return (n > 1) ? fibonacci(n - 2) + fibonacci(n - 1) : n;
}
console.time('fibonacci');
console.log(fibonacci(30));
console.timeEnd('fibonacci');
```

##### console.dir()
```javascript
console.dir(console);
```

##### console.table()
```javascript
var people = [
    {
        name: 'Hopper', surname: 'Herring'
    }, {
        name: 'Sampson', surname: 'Douglas'
    }, {
        name: 'Carmella', surname: 'Vincent'
    }
];
console.table(people);
console.table(
    document.getElementsByTagName('a'),
    ['href', 'text']
);
```

##### debugger;
```javascript
(function() {
    debugger;
})();
console.log(__commandLineAPI);
```

##### __commandLineAPI
```javascript
var members = Object.keys(__commandLineAPI).filter(function(key) {
    return ! (key in console);
}).reduce(function(obj, key) {
   obj[key] = __commandLineAPI[key];
   return obj;
}, {});
console.dir(members);
```
