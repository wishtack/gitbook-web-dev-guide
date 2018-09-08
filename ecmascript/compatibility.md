# Compatibility

How can we use the latest ECMAScript features and still be compatible with most browsers?

[https://kangax.github.io/compat-table/es6/](https://kangax.github.io/compat-table/es6/)

{% embed data="{\"url\":\"https://kangax.github.io/compat-table/es6/\",\"type\":\"link\",\"title\":\"ECMAScript 6 compatibility table\",\"icon\":{\"type\":\"icon\",\"url\":\"https://kangax.github.io/compat-table/favicon.ico\",\"aspectRatio\":0}}" %}

## Transpilation

ECMAScript 5.1 is for modern ECMAScript what assembly is for C++.

We need a transpiler:

* Babel: [https://babeljs.io/](https://babeljs.io/)​
* TypeScript: [https://www.typescriptlang.org/](https://www.typescriptlang.org/)​

But this will not be enough as transpilers will only convert syntactic features but not new browser APIs and methods.

## Polyfills

We need to compensate the lack of some objects, functions or methods `customElements`, `fetch`, `Array.filter` on some browsers.

In order to fill the gap, we will use polyfill libraries. These libraries detect missing features and compensate them with **JavaScript implementations**.

Example:

```javascript
if (Array.prototype.first == null) {
    Array.prototype.first = function () {
        return this[0];
    };
}
​
const valueList = [1, 2, 3];
​
console.log(valueList.first()); // 1
```

One of the most famous polyfill libraries is core-js [https://github.com/zloirock/core-js](https://github.com/zloirock/core-js).

Or you can use a polyfill service like [https://polyfill.io](https://polyfill.io).

