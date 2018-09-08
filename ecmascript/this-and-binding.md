# this & "binding"

## Who am I?

{% tabs %}
{% tab title=" 🧐" %}
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
        setTimeout(function () {
            this.sayHi();
        }, 1000);
    }
​
}
​
const customer = new Customer('Foo', 'BAR');
​
customer.sayHiLater(); // ???
```
{% endtab %}

{% tab title=" 😱" %}
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
        setTimeout(function () {
            this.sayHi();
        }, 1000);
    }
​
}
​
const customer = new Customer('Foo', 'BAR');
​
customer.sayHiLater(); // TypeError: this.sayHi is not a function
```
{% endtab %}
{% endtabs %}

## Binding

The callback function given to `setTimeout` is not bound to our `Customer` instance. In addition to this, `setTimeout` tries to help us by binding the timeout objet _\(which is as well returned by setTimeout\)_ to our callback function.

```javascript
const const timeout = setTimeout(function () {
    console.log(this === timeout); // true
});
```

In order to fix this issue, we should bind our instance of `Customer` to callback function.

### The hacky way {#the-hacky-way}

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
        setTimeout(function () {
            this.sayHi();
        }.bind(this), 1000);
    }
​
}
```

### The other hacky way {#the-other-hacky-way}

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
        const _this = this;
        setTimeout(function () {
            _this.sayHi();
        }, 1000);
    }
​
}
```

### The clean way

See you at the [next chapter](arrow-functions.md).

