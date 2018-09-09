# Element Modification

Once you retrieve the reference to an element in the DOM, you can modify any of the element's properties.

### Modify content

```javascript
element.textContent = 'Hello 🌏';
```

{% hint style="warning" %}
HTML content can be controlled using `element.innerHTML` attribute but this approach is dangerous as it can lead to **XSS** _**\(Cross-Site Scripting\)**_ **vulnerabilities**.

In addition to the security issues, updating the `innerHTML` forces the browser to parse the HTML then update the DOM content. This can have bad performance results.
{% endhint %}

### Modify properties

```javascript
/* Toggle `disabled` state. */
button.disabled = !button.disabled;

link.src = `https://wishtack.io`;
```

### Modify the structure

#### Create a DOM element

```javascript
const child = document.createElement('div');
```

#### Append an element

```javascript
parent.appendChild(child);
```

#### Remove an element

```javascript
parent.removeChild(child);
```

### CSSOM _\(CSS Object Model\)_

```javascript
/* Update some CSS style. */
element.style.backgroundColor = 'red';

/* Added a CSS class to an element. */
element.classList.add('blog-post-content');

/* Toggle a CSS class. */
element.classList.toggle('important');
```



