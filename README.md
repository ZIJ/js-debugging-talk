js-debugging-talk
=================

Code snippeds for my "Debugging JS with Chrome" talk at FDC'14

##### Logging, warnings, errors and assertion
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

##### Counting keypresses
```javascript
document.addEventListener('keydown', function(event) {
  console.count(String.fromCharCode(event.keyCode));
});
```

##### Measuring performance of [ineffecient] Fibonacci number calculation
```javascript
function fibonacci(n) {
  return (n > 1) ? fibonacci(n - 2) + fibonacci(n - 1) : n;
}
console.time('fibonacci');
console.log(fibonacci(30));
console.timeEnd('fibonacci');
```
