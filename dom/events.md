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

These events can be intercepted by adding an **event listener** to the corresponding event type.

An event listener is a JavaScript function that **will be called whenever the event is triggered**.

In most cases, the listener function will take as first argument, **the event object** with different properties and data depending on the event type and the event itself.

