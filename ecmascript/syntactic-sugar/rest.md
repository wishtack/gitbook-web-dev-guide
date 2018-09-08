# Rest

## Array Rest

Rest parameters are the equivalent for variadic parameters in some other languages.

The `add` function below can take any number of parameters which will end up in the `valueList` `Array`.

```javascript
const add = (...valueList) => {
    return valueList.reduce((total, value) => total + value, 0);
};

add(0, 1, 2, 3); // 6
```

{% hint style="warning" %}
It is better to avoid the usage of "rest" parameters.  
It reduces the extensibility of the function. It is better to use one parameter of type `Array` that contains all the values.

```typescript
const add = (valueList) => {
    return valueList.reduce((total, value) => total + value, 0);
};

add([1, 2, 3]); // 6
```
{% endhint %}

## Object Rest

The same syntax can be used with the [destructuring](destructuring.md#object-destructuring) of an object.

```javascript
const user = {
    firstName: 'Foo',
    lastName: 'BAR',
    email: 'foo.bar@wishtack.com',
    phoneNumber: '123'
};

const { firstName, lastName, ...remainingProperties } = user;

console.log(remainingProperties); // { email: 'foo.bar@wishtack.com', phoneNumber: '123' }

```



