# The Event Loop

The Event Loop Behavior

What's the execution order of this code?

{% tabs %}
{% tab title=" 🧐" %}
```javascript
var value;
​
setTimeout(function () {
    value = 'VALUE';
}, 100 /* 100 ms. */);
​
console.log(value); // ???
​
setTimeout(function () {
    console.log(value); // ???
}, 200);
```
{% endtab %}

{% tab title="👍" %}
```javascript
var value;
​
setTimeout(function () {
    value = 'VALUE';
}, 100 /* 100 ms. */);
​
console.log(value); // 1 - undefined
​
setTimeout(function () {
    console.log(value); // 2 - VALUE
}, 200);
```
{% endtab %}
{% endtabs %}

And in this case?

{% tabs %}
{% tab title=" 🧐" %}
```javascript
function main() {
​
    var value;
​
    setTimeout(function () {
        value = 'VALUE';
    }, 0 /* 0 ms. */);
​
    console.log(value); // ???
​
    setTimeout(function () {
        console.log(value); // ???
    }, 0);
    
    console.log(value); // ???
​
}
​
main();
```
{% endtab %}

{% tab title="👍" %}
```javascript
function main() {
​
    var value;
​
    setTimeout(function () {
        value = 'VALUE';
    }, 0 /* 0 ms. */);
​
    console.log(value); // 1 - undefined
​
    setTimeout(function () {
        console.log(value); // 3 - VALUE
    }, 0);
    
    console.log(value); // 2 - undefined
    
}
​
main();
```
{% endtab %}
{% endtabs %}

## How the event loop works

1. **Register a listener** : Most asynchronous tasks requires the definition of a callback function in order to retrieve the result of the processing or simply in order to know that the processing ended. During this step, we explicitly or implicitly subscribe a listener to some event source. Examples: `setTimeout`, `addEventListener` etc...
2. **Add the function to the queue**: The callback function cannot be called immediately when the result is received as the thread might be busy executing another function. In the example below, both callback functions are ready to be called the thread is busy executing our `main` function. The JavaScript engine adds references to the callback functions at the end of the callback queue in order to be called once the thread is free.
3. **Tick** : When the `main` function execution ends, the thread won't have time to stay idle and will immediately grab the callback at the top of the queue and execute it. More precisely, this is the event loop which simply loops forever executing every function in the queue. **The moment where the event loop ends the execution of a function and is ready to grab the next one is called a "tick"**.

![The event loop](../.gitbook/assets/event-loop.jpg)

{% embed data="{\"url\":\"https://www.youtube.com/watch?v=8aGhZQkoFbQ\",\"type\":\"video\",\"title\":\"Philip Roberts: What the heck is the event loop anyway? \| JSConf EU 2014\",\"description\":\"JavaScript programmers like to use words like, “event-loop”, “non-blocking”, “callback”, “asynchronous”, “single-threaded” and “concurrency”.\\n\\nWe say things like “don’t block the event loop”, “make sure your code runs at 60 frames-per-second”, “well of course, it won’t work, that function is an asynchronous callback!”\\n\\nIf you’re anything like me, you nod and agree, as if it’s all obvious, even though you don’t actually know what the words mean; and yet, finding good explanations of how JavaScript actually works isn’t all that easy, so let’s learn!\\n\\nWith some handy visualisations, and fun hacks, let’s get an intuitive understanding of what happens when JavaScript runs.\\n\\nTranscript: http://2014.jsconf.eu/speakers/philip-roberts-what-the-heck-is-the-event-loop-anyway.html\\n\\nLicense: For reuse of this video under a more permissive license please get in touch with us. The speakers retain the copyright for their performances.\",\"icon\":{\"type\":\"icon\",\"url\":\"https://www.youtube.com/yts/img/favicon\_144-vfliLAfaB.png\",\"width\":144,\"height\":144,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://i.ytimg.com/vi/8aGhZQkoFbQ/maxresdefault.jpg\",\"width\":1280,\"height\":720,\"aspectRatio\":0.5625},\"embed\":{\"type\":\"player\",\"url\":\"https://www.youtube.com/embed/8aGhZQkoFbQ?rel=0&showinfo=0\",\"html\":\"<div style=\\\"left: 0; width: 100%; height: 0; position: relative; padding-bottom: 56.2493%;\\\"><iframe src=\\\"https://www.youtube.com/embed/8aGhZQkoFbQ?rel=0&amp;showinfo=0\\\" style=\\\"border: 0; top: 0; left: 0; width: 100%; height: 100%; position: absolute;\\\" allowfullscreen scrolling=\\\"no\\\"></iframe></div>\",\"aspectRatio\":1.7778},\"caption\":\"What the heck is the event loop anyway?\"}" %}



