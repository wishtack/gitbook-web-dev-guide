# Named Parameters

Ordered parameters can make the code harder to read and refactor.

```javascript
class Customer {
    constructor(firstName, lastName, email, phoneNumber) {
        this.firstName = firstName;
        this.lastName = lastName;
        this.email = email;
        this.phoneNumber = phoneNumber;
    }
}
​
new Customer('Foo', null, null, '123');
```

Unluckily, named parameters do not exist in JavaScript but there is a native workaround thanks to destructuring.

## Named Parameters with one parameter

```javascript
class Customer {
    constructor(args) {
        this.firstName = args.firstName;
        this.lastName = args.lastName;
        this.email = args.email;
        this.phoneNumber = args.phoneNumber;
    }
}
​
new Customer({
    firstName: 'Foo',
    phoneNumber: '123'
});
```

But this is not very IDE-friendly and without reading the content of the constructor, there's no way to know what are the expected parameters.

## Destructuring

The destructuring can be used in the constructor's _\(or any other function\)_ parameters description.

```javascript
class Customer {
    constructor({firstName, lastName, email, phoneNumber = null} = {}) {
        this.firstName = firstName;
        this.lastName = lastName;
        this.email = email;
        this.phoneNumber = phoneNumber;
    }
}
```

Which is a shorthand for:

```javascript
class Customer {
    constructor(args = {}) {
    
        const {firstName, lastName, email, phoneNumber = null} = args;
    
        this.firstName = firstName;
        this.lastName = lastName;
        this.email = email;
        this.phoneNumber = phoneNumber;
    }
}
```

## Recycling

For simple objects, this constructor can be used as is without having to implement factories for handling copy or deserialization.

```javascript
const customer = new Customer({firstName: 'Foo'});
​
const customerFromJson = new Customer(JSON.parse(data));
​
const customerCopy = new Customer(customer);
```



##  

