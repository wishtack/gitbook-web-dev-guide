# Classes

## ES6 Classes

{% tabs %}
{% tab title="ES6 Class" %}
```javascript
class Customer {

    constructor(firstName, lastName) {
        this.firstName = firstName;
        this.lastName = lastName;
    }
    
    getName() {
        return this.firstName;
    }

}
```
{% endtab %}

{% tab title="Legacy Prototype" %}
```javascript
var Customer = function(firstName, lastName) {
    this.firstName = firstName;
    this.lastName = lastName;
}

Customer.prototype = {
    getName: function () {
        return this.firstName;
    }
}
```
{% endtab %}
{% endtabs %}

## Visibility

Meanwhile [class fields](https://github.com/tc39/proposal-class-fields) get supported, visibility rules are just based on a common naming convention where properties and methods get prefixed with the underscore character `_` if they are private.

```javascript
class Customer {

    constructor(firstName, lastName) {
        this.firstName = firstName;
        this.lastName = lastName;
        this.email = null;
        this._isBadPayer = this._tellIfBadPayer();
    }
    
    getName() {
        return this.firstName;
    }
    
    _tellIfBadPayer() {
        return this.firstName === 'foo';
    }

}
```

## Properties

```javascript
class Customer {

    constructor(firstName, lastName) {
        this.firstName = firstName;
    }

    get firstName() {
        return this._firstName;
    }
    
    set firstName(value) {
        this._firstName = value;
    }
    
}

/* @HACK: Last time we use var, I promise! */
var customer = new Customer();

customer.firstName = 'Foo';

console.log(customer.firstName); // Foo
```

{% hint style="danger" %}
Avoid using properties.

Properties can become handy in some extreme cases like the integration of some legacy library, mock, implementing a runtime type checking decorator or something fancy like that etc...

Otherwise, properties will only introduce ambiguity.

Who would imagine that this code might trigger a runtime exception?

```javascript
var customer = new Customer();
element.textContent = customer.name;
```

Or even worse, things might end up like this:

```javascript
/* @HACK: Do not remove this useless line as it initializes
 * the user eagerly instead of running it lazily. */
request.user;
```
{% endhint %}

## Inheritance

This is inheritance:

```javascript
export class WishtackProduct extends Product {

    ...

    getProductId() {
        return 'wishtack-' + this._wishtackId;
    }

}
```

{% hint style="warning" %}
Now, avoid it...

... and prefer composition!
{% endhint %}



