# Fetch Web API

{% hint style="warning" %}
Luckily, thanks to the `fetch` Web API and without any external library, we will not need to use the old fashioned `XMLHttpRequest` object.

```javascript
const xmlHttpRequest = new XMLHttpRequest();

xmlHttpRequest.onreadystatechange = () => {
    if (xmlHttpRequest.readyState === 4 /* request is complete */
        && xmlHttpRequest.status === 200) {
        document.querySelector('.wt-wish-list').innerHTML = xmlHttpRequest.responseText;
    }
};

xmlHttpRequest.open('GET', '/users/123456/wishes/', true /* async */);

xmlHttpRequest.send();
```
{% endhint %}

## `fetch` usage

The `fetch()` function returns a `Promise<Response>` _\(a promise that resolves to a `Response` object\)_.

The `Response.json()` method returns a `Promise` that resolves the object produced by parsing the JSON content of the body.

```javascript
fetch('https://www.googleapis.com/books/v1/volumes?q=extreme%20programming')
    .then(response => response.json())
    .then(data => console.log(data));
```

Or using `async/await`:

```javascript
const response = await fetch('https://www.googleapis.com/books/v1/volumes?q=extreme%20programming');
const data = await response.json();
console.log(data);
```

## `fetch` options

The **second argument** for the `fetch` function is an **options object** that allows you for instance to send `POST` requests or to control additional stuff in the request like HTTP headers.

```javascript
const book = {
    id: 'BOOK_ID',
    title: 'eXtreme Programming explained'
};

fetch('https://api.mylibrary.io/books', {
    method: 'GET',
        headers: {
            'Content-Type': 'application/json; charset=utf-8'
        },
        body: JSON.stringify(book)
});
```

{% hint style="warning" %}
In order to avoid security issues like URL forgery, it is recommended to encode the dynamic parts of the URL when constructing it using the `encodeURIComponent` function.

```javascript
const uri = `https://api.mylibrary.io/books/${encodeURIComponent(bookId)}`;
```
{% endhint %}



