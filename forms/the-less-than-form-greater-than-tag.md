# The &lt;form&gt; tag

## `<form>` tag attributes

The first step when implementing an HTML form is to add a `form` tag.

```markup
<form>
...
</form>
```

The form tag has three main attributes:

* **action**: that describes the URL where the data should be sent when the form is submitted.
* **enctype**: that specifies the encoding to use for sending data _\(`application/x-www-form-urlencoded`, `multipart/form-data` and `text/plain`\)_. 
* **method**: that controls the HTTP method that will be used to send data to server.

## Example

```markup
<form
    method="post"
    enctype="application/x-www-form-urlencoded"
    action="https://mylibrary.io/books">
</form>
```

## Intercepting `submit` event

In most cases in a JavaScript application, the content shouldn't be sent directly over the network to the backend but it **should be intercepted by the JavaScript** on submission.

When the user submits the form _\(e.g.: presses enter or clicks on a `<button type="submit">` inside the form\)_, the `form` element triggers a `submit` event.

The JavaScript can be intercepted by adding an event listener and the default behavior _\(sending the form's data to the backend\)_ disabled calling the `preventDefault` method on the event.

```javascript
const form = document.querySelector('form');

form.addEventListener('submit', submitEvent => {
    submitEvent.preventDefault();
    ...
});
```



