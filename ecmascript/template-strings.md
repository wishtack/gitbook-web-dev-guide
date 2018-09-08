# Template Strings

```javascript
const appName = 'Wishtack';
const userName = 'Foo';
const greetings = `Hi ${userName},
Welcome to ${appName}!`
​
console.log(greetings);
​
// Result:
// Hi Foo,
// Welcome to Wishtack!
```

{% hint style="danger" %}
**Security** **Warning**

Template strings is not an HTML templating tool.  
Using template strings to produce HTML might expose you to XSS _\(Cross-Site Scripting\)_ vulnerabilities.

Vulnerable example:

```javascript
/* userName is dynamically retrieved from malicious source:
 * query string, api, storage etc... */
const userName = '<img src=404 onerror=alert(1)>'; 
document.body.innerHTML = `<span>Hi ${userName}</span>`
```
{% endhint %}



