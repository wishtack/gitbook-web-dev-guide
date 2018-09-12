# Injection

Web applications are mainly exposed to **HTML and JavaScript code injection**.

There are multiple entry points:

* Some part of the URL,
* Parameters,
* Data coming from an "unsafe" API.

{% hint style="info" %}
Third-party _\(user, partner etc...\)_ data should not be trusted and never executed or used as an HTML template.
{% endhint %}

{% hint style="danger" %}
Never use `eval().`
{% endhint %}

### Encode URI components

When constructing a URL, dynamic parts should be URI encoded.

```javascript
const url = `https://api.wishtack.com/users/${encodeURIComponent(userId)}`;
```

