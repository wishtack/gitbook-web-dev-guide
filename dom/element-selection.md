# Element Selection

## Old School

### Selecting an element by id

```javascript
document.getElementById('login');
```

This code will return the first element having the given id.

```markup
<input id="login">
```

### Select using CSS class

```javascript
document.getElementsByClassName('blog-post');
```

This code will return the first element having the `blog-post-content` CSS class.

```markup
<section class="blog-post-content"></section>
```

### Select by HTML tag

```javascript
document.getElementsByTagName('header')
```

This code will return the first element having the `header` HTML tag.

```markup
<header>This is the header.</header>
```

## Modern Way

### Select using query selector

```javascript
document.querySelector('header');
document.querySelectorAll('div.blog-post-content');
```

The first call will return the first element with the header HTML tag.

The second call will return an iterable object with all the items with a `div` HTML tag and the `blog-post-content` CSS class.

{% hint style="success" %}
This is the easier and most modern way of selecting elements.
{% endhint %}

{% hint style="info" %}
`querySelector` and `querySelectorAll` methods are also available on every element in order to search for child elements.

```javascript
const firstNameInput = form.querySelector('input[name="firstName"]');
```
{% endhint %}

