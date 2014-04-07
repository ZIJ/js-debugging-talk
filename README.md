js-debugging-talk
=================

Code snippeds for my "Debugging JS with Chrome" talk at FDC'14

##### The basics

```javascript
var obj = { prop: 1, child: { prop: 2 } };
console.log(obj);
console.log('%O\n%o', document.body, document.body);
console.warn('something unexpected happened');
console.error('something went wrong');
console.assert("str" instanceof String, 'gotcha!');
```
