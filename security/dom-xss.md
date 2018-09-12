# DOM XSS

If a user can control the executed code or HTML, a malicious user can **send a crafted URL to a victim and control the executed code**.

### Vulnerable code examples

{% hint style="danger" %}
```javascript
eval(document.querySelector('input[name="expression"]').value);
```
{% endhint %}

{% hint style="danger" %}
```javascript
const firstName = document.querySelector('input[name="firstName"]').value;
document.querySelector('.wt-first-name').innerHTML = firstName;
```
{% endhint %}

#### ECMAScript Template String

ECMAScript template strings should not be used for HTML templating.

{% hint style="danger" %}
```javascript
element.innerHTML = `<div>Hi, ${firstName}</div>`;
```
{% endhint %}

Where `firstName` might be controlled by a malicious user.

{% hint style="danger" %}
Except the application's code, every external source should be considered harmful.
{% endhint %}

{% hint style="success" %}
User your frameworks escaping features.
{% endhint %}

