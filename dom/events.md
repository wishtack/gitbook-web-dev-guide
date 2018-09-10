# Events

Modern browsers can trigger **hundreds of types of events** _\(~500\)_.

[https://developer.mozilla.org/en-US/docs/Web/Events](https://developer.mozilla.org/en-US/docs/Web/Events)

{% embed data="{\"url\":\"https://developer.mozilla.org/en-US/docs/Web/Events\",\"type\":\"link\",\"title\":\"Event reference\",\"description\":\"DOM Events are sent to notify code of interesting things that have taken place. Each event is represented by an object which is based on the Event interface, and may have additional custom fields and/or functions used to get additional information about what happened. Events can represent everything from basic user interactions to automated notifications of things happening in the rendering model.\",\"icon\":{\"type\":\"icon\",\"url\":\"https://developer.mozilla.org/static/img/favicon144.e7e21ca263ca.png\",\"width\":144,\"height\":144,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://developer.mozilla.org/static/img/opengraph-logo.72382e605ce3.png\",\"width\":600,\"height\":600,\"aspectRatio\":1}}" %}

These event types can be of any kind:

* User interaction : click, input change, keypress, drag & drop etc...
* Geolocation,
* Device motion,
* Network status,
* ...

## Registering Event Listeners

These events can be intercepted by adding an **event listener** to the corresponding event type.

An event listener is a JavaScript function that **will be called whenever the event is triggered**.

In most cases, the listener function will take as first argument, **the event object** with different properties and data depending on the event type and the event itself.

### Listening to a click

```javascript
const button = document.querySelector('button');

let clickCount = 0;

/* Increment the counter on every click. */
button.addEventListener('click', () => clickCount++);
```

### Listening to keyboard

```javascript
document.addEventListener('keydown', event => {
    if (event.ctrlKey === true
        && event.key === 'x'
        /* This will show a confirmation dialog and return true if user confirms. */
        && confirm('Do you really want to remove the selected blog post?')) {
        removeSelectedItem();
    }
});
```

### Watching geolocation

```javascript
navigator.geolocation.watchPosition(position => {
    console.log(`
    Accuracy: ${position.coords.accuracy},
    Latitude: ${position.coords.latitude},
    Longitude: ${position.coords.longitude}
    `);
});
```

{% hint style="info" %}
Some functions like `watchPosition` will prompt the user for his consent before allowing access to geolocation.
{% endhint %}

## Removing Event Listeners

In order to avoid **side effects**, **dead code** and **memory leaks** it is important to think about clearing your event registrations by removing the listeners.

This can be done differently depending on the event type.

#### `removeEventListener`

```javascript
const listener = () => clickCount++;

button.addEventListener('click', listener);

button.removeEventListener('click', listener);
```

#### `clear...`

```javascript
const watchId = navigator.geolocation.watchPosition(...);
navigator.geolocation.clearWatch(watchId);

const interval = setInterval(() => console.log(clickCount), 1000);
clearInterval(interval);
```

## Events bubbling & capturing

[http://javascript.info/bubbling-and-capturing](http://javascript.info/bubbling-and-capturing)

{% embed data="{\"url\":\"http://javascript.info/bubbling-and-capturing\",\"type\":\"link\",\"title\":\"Bubbling and capturing\",\"icon\":{\"type\":\"icon\",\"url\":\"http://javascript.info/img/favicon/apple-touch-icon-precomposed.png\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://javascript.info/img/site\_preview\_en\_1200x630.png\",\"width\":1200,\"height\":630,\"aspectRatio\":0.525}}" %}

