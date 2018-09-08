# Arrow Functions

```javascript
/* 90s */
function sayHi(userName) {
    console.log('Hi ' + userName);
}
​
/* 2000s */
var sayHi = function (userName) {
    console.log('Hi ' + userName);
};
​
/* 2015 */
const sayHi = (userName) => {
    console.log('Hi ' + userName);
});
```

## No binding

 Arrow functions cannot be bound to objects. The `this` variable's value will always be the one of the parent closure.

```javascript
class Customer {
​
    constructor(firstName, lastName) {
        this.firstName = firstName;
        this.lastName = lastName;
    }
    
    sayHi() {
        console.log('Hi ' + this.firstName);
    }
    
    sayHiLater() {
        setTimeout(() => {
            this.sayHi();
        }, 1000);
    }
​
}
```

## Example with `Array.filter` and `Array.map`

```javascript
const productList = [
    {
        title: 'Browserstack',
        price: 50
    },
    {
        title: 'Keyboard',
        price: 20
    },
    {
        title: 'Prerender',
        price: 10
    }
];
​
const cheapProductList = productList.filter((product) => {
    return product.price < 25;
});
​
const cheapProductTitleList = cheapProductList.map((product) => {
    return product.title;
});
​
console.log(cheapProductTitleList); // ['Keyboard', 'Prerender']
```

## One-liner

In most cases, callbacks are just simple one-liners.

In this case, curly braces `{}` and the `return` statement can be removed.

If the arrow function only takes one parameter, the parentheses `()` can be removed.

```javascript
const cheapProductTitleList = productList
    .filter(product => product.price < 25)
    .map(product => product.title);
```

{% hint style="warning" %}
In case of variable name shadowing, try to avoid single letter variable names or generic names.

`filter(u => u.id === user.id)`

`filter(it => it.id === user.id)`
{% endhint %}

{% hint style="success" %}
Prefer the `_` prefix to mark the difference between the local variable and the one from the parent closure.

`filter(_user => _user.id === user.id)`
{% endhint %}

