# Hoisting is Dead: var vs. let vs. const

## Reminder

### Global variables 🤮

```javascript
userName = 'Foo BAR';

console.log(userName); // Foo BAR
```

### Use strict 😅

```javascript
'use strict';

userName = 'Foo BAR'; // ReferenceError: userName is not defined
```

```javascript
'use strict';

console.log(userName); // ReferenceError: userName is not defined
```

## Hoisting

### Variable hoisting

{% tabs %}
{% tab title="🧐" %}
```javascript
'use strict';

console.log(userName); // ???

var userName = 'Foo BAR';
```
{% endtab %}

{% tab title="😱" %}
```javascript
'use strict';

console.log(userName); // undefined

var userName = 'Foo BAR';
```
{% endtab %}
{% endtabs %}

### Function hoisting

{% tabs %}
{% tab title="🧐" %}
```javascript
'use strict';

greetings(); // ???

function greetings() {
    console.log('HI!');
}

function greetings() {
    console.log('HELLO!');
}
```
{% endtab %}

{% tab title="😱" %}
```javascript
'use strict';

greetings(); // HELLO!

function greetings() {
    console.log('HI!');
}

function greetings() {
    console.log('HELLO!');
}
```
{% endtab %}
{% endtabs %}

### A little bit better

```javascript
'use strict';

greetings(); // TypeError: greetings is not a function.

var greetings = function () {
    console.log('HI!');
};

greetings(); // HI!

var greetings = function () {
    console.log('HELLO!');
};

greetings(); // HELLO!
```

## let

Variables are only accessible after their declaration.

```javascript
console.log(userName); // ReferenceError: userName is not defined

let userName = 'Foo BAR';
```

Variables are only accessible in the bloc where they are declared.

```javascript
if (true) {
    let userName = 'Foo BAR';
}

console.log(userName); // ReferenceError: userName is not defined
```

## const

`const` variables cannot be reinitialized.

```javascript
const user = {
    firstName: 'Foo',
    lastName: 'BAR'
}

user = null; // TypeError: Assignment to constant variable.
```

{% hint style="warning" %}
`const` does not mean immutable.

```javascript
user.firstName = 'John'; // OK!
```
{% endhint %}

{% hint style="success" %}
It is recommended to declare all variables as `const` except if reusing the variable is inevitable.

This is less error-prone and avoids some common inattention mistakes.

`const` usage avoids clumsy variable reuse:

```javascript
const user = {
    firstName: 'Foo',
    lastName: 'BAR'
}

/* 🤢*/
user = user.firstName; // TypeError: Assignment to constant variable.
```
{% endhint %}

