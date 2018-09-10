# Transitions

Transforms are a bit rough. They need some smoothness. Let's animate them!

```css
.wt-demo-transform {
    border-style: solid;
    border-width: 1px;
    margin: auto;
    padding: 10px;
    width: 100px;

    transition: transform .5s;
}

.wt-demo-transform:hover {
    transform: perspective(100px) rotateY(405deg);
}
```

[https://codepen.io/younes-jaaidi/pen/qMxpxY](https://codepen.io/younes-jaaidi/pen/qMxpxY)

{% embed data="{\"url\":\"https://codepen.io/younes-jaaidi/pen/qMxpxY\",\"type\":\"rich\",\"title\":\"web-dev-css-3d-transition\",\"description\":\"...\",\"icon\":{\"type\":\"icon\",\"url\":\"https://codepen.io/favicons/favicon-192x192.png\",\"width\":192,\"height\":192,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://s3-us-west-2.amazonaws.com/m.cdpn.io/screenshot-coming-soon-small.png\",\"width\":400,\"height\":225,\"aspectRatio\":0.5625},\"embed\":{\"type\":\"app\",\"url\":\"https://codepen.io/younes-jaaidi/embed/preview/qMxpxY?height=300&slug-hash=qMxpxY&default-tabs=css,result&host=https://codepen.io&embed-version=2\",\"html\":\"<iframe src=\\\"https://codepen.io/younes-jaaidi/embed/preview/qMxpxY?height=300&amp;slug-hash=qMxpxY&amp;default-tabs=css,result&amp;host=https://codepen.io&amp;embed-version=2\\\" style=\\\"border: 0; width: 100%; height: 300px;\\\" allowfullscreen></iframe>\",\"height\":300,\"aspectRatio\":null}}" %}

The `transition` property takes 4 parameters:

1. The property we want to animate.
2. Transition duration.
3. Timing function _\(ease, linear, ease-in, ease-out, ease-in-out, cubic-bezier\)_.
4. Delay to apply before starting the transition.

### Multiple transitions

It is possible to apply transitions on multiple properties with different parameters.

```css
.wt-demo-transition {
    border-style: solid;
    border-width: 1px;
    margin: auto;
    padding: 10px;

    height: 18px;
    width: 73px;

    transition: height 1s ease-in, width 1s ease-out 1s;
}

.wt-demo-transition:hover {
    height: 118px;
    width: 173px;
}
```

[https://codepen.io/younes-jaaidi/pen/aaqEKq](https://codepen.io/younes-jaaidi/pen/aaqEKq)

{% embed data="{\"url\":\"https://codepen.io/younes-jaaidi/pen/aaqEKq\",\"type\":\"rich\",\"title\":\"web-dev-css-transition-multi-property\",\"description\":\"...\",\"icon\":{\"type\":\"icon\",\"url\":\"https://codepen.io/favicons/favicon-192x192.png\",\"width\":192,\"height\":192,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://s3-us-west-2.amazonaws.com/m.cdpn.io/screenshot-coming-soon-small.png\",\"width\":400,\"height\":225,\"aspectRatio\":0.5625},\"embed\":{\"type\":\"app\",\"url\":\"https://codepen.io/younes-jaaidi/embed/preview/aaqEKq?height=300&slug-hash=aaqEKq&default-tabs=css,result&host=https://codepen.io&embed-version=2\",\"html\":\"<iframe src=\\\"https://codepen.io/younes-jaaidi/embed/preview/aaqEKq?height=300&amp;slug-hash=aaqEKq&amp;default-tabs=css,result&amp;host=https://codepen.io&amp;embed-version=2\\\" style=\\\"border: 0; width: 100%; height: 300px;\\\" allowfullscreen></iframe>\",\"height\":300,\"aspectRatio\":null}}" %}

{% hint style="success" %}
For better user experience, use short transitions _\(less than 500ms\)_.
{% endhint %}



