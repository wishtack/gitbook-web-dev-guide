# Element Modification

Once you retrieve the reference to an element in the DOM, you can modify any of the element's properties.

#### Modify content

```javascript
element.textContent = 'Hello 🌏';
```

#### Modify properties

```javascript
/* Toggle `disabled` state. */
button.disabled = !button.disabled;

link.src = `https://wishtack.io`;
```

#### CSSOM _\(CSS Object Model\)_

```javascript
/* Update some CSS style. */
element.style.backgroundColor = 'red';

/* Added a CSS class to an element. */
element.classList.add('blog-post-content');

/* Toggle a CSS class. */
element.classList.toggle('important');
```



