# Form validation

## Type

The `type` attribute of the `<input>` elements describes the behavior and validation constraints of the input.

[http://www.w3schools.com/html/html\_form\_input\_types.asp](http://www.w3schools.com/html/html_form_input_types.asp)

{% embed data="{\"url\":\"http://www.w3schools.com/html/html\_form\_input\_types.asp\",\"type\":\"link\",\"title\":\"HTML Input Types\",\"description\":\"Well organized and easy to understand Web building tutorials with lots of examples of how to use HTML, CSS, JavaScript, SQL, PHP, and XML.\",\"icon\":{\"type\":\"icon\",\"url\":\"https://www.w3schools.com/favicon.ico\",\"aspectRatio\":0}}" %}

{% hint style="info" %}
On some devices, the virtual keyboard will be adapted to the type of the input.
{% endhint %}

## Validation

By default, a form **can not be submitted until all inputs are valid**.

It is possible to use additional attributes like `maxlength`, `minlength`, `pattern` or `required` to **apply some additional constraints**.

The `validity` property of the `<input>` element can be used in JavaScript to check input's validity and eventually, the invalidity reason.

```javascript
const input = document.querySelector('input');

input.validity.valid; // false
input.validity.valueMissing; // true
```

{% hint style="info" %}
It is possible to disable native validation using the form's `novalidate` attribute.

This can be used to validate the form manually or using a JavaScript library or framework.
{% endhint %}



