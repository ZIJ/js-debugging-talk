js-debugging-talk
=================

Code snippeds for my "Debugging JS with Chrome" talk at FDC'14

##### Logging, warnings, errors and assertion
```javascript
var obj = { prop: 1, child: { prop: 2 } };
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
