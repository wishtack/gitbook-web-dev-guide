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



