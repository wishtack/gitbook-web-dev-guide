# Transforms

## 2D transforms

2D transforms modify position, rotation and size of elements using CSS.

### Example - Rotating an element on hover

```css
.wt-demo-transform {
    border-style: solid;
    border-width: 1px;
    height: 20px;
    width: 100px;
    margin: auto;
}

.wt-demo-transform:hover {
    transform: rotate(180deg) scale(2);
}
```

[https://codepen.io/younes-jaaidi/pen/mGXpPz](https://codepen.io/younes-jaaidi/pen/mGXpPz)

{% embed data="{\"url\":\"https://codepen.io/younes-jaaidi/pen/mGXpPz\",\"type\":\"rich\",\"title\":\"web-dev-css-2d-transform\",\"description\":\"...\",\"icon\":{\"type\":\"icon\",\"url\":\"https://codepen.io/favicons/favicon-192x192.png\",\"width\":192,\"height\":192,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://s3-us-west-2.amazonaws.com/m.cdpn.io/screenshot-coming-soon-small.png\",\"width\":384,\"height\":225,\"aspectRatio\":0.5859375},\"embed\":{\"type\":\"app\",\"url\":\"https://codepen.io/younes-jaaidi/embed/preview/mGXpPz?height=300&slug-hash=mGXpPz&default-tabs=css,result&host=https://codepen.io&embed-version=2\",\"html\":\"<iframe src=\\\"https://codepen.io/younes-jaaidi/embed/preview/mGXpPz?height=300&amp;slug-hash=mGXpPz&amp;default-tabs=css,result&amp;host=https://codepen.io&amp;embed-version=2\\\" style=\\\"border: 0; width: 100%; height: 300px;\\\" allowfullscreen></iframe>\",\"height\":300,\"aspectRatio\":null}}" %}

## 3D transforms

### Example - Rotating an element around the Y axis on hover with a perspective effect

```css
.wt-demo-transform {
    border-style: solid;
    border-width: 1px;
    width: 100px;
    margin: auto;
    padding: 10px;
}

.wt-demo-transform:hover {
    transform: perspective(100px) rotateX(10deg) rotateY(45deg);
}
```

[https://codepen.io/younes-jaaidi/pen/XPZVgg](https://codepen.io/younes-jaaidi/pen/XPZVgg)

{% embed data="{\"url\":\"https://codepen.io/younes-jaaidi/pen/XPZVgg\",\"type\":\"rich\",\"title\":\"web-dev-css-3d-transform\",\"description\":\"...\",\"icon\":{\"type\":\"icon\",\"url\":\"https://codepen.io/favicons/favicon-192x192.png\",\"width\":192,\"height\":192,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://s3-us-west-2.amazonaws.com/m.cdpn.io/screenshot-coming-soon-small.png\",\"width\":400,\"height\":225,\"aspectRatio\":0.5625},\"embed\":{\"type\":\"app\",\"url\":\"https://codepen.io/younes-jaaidi/embed/preview/XPZVgg?height=300&slug-hash=XPZVgg&default-tabs=css,result&host=https://codepen.io&embed-version=2\",\"html\":\"<iframe src=\\\"https://codepen.io/younes-jaaidi/embed/preview/XPZVgg?height=300&amp;slug-hash=XPZVgg&amp;default-tabs=css,result&amp;host=https://codepen.io&amp;embed-version=2\\\" style=\\\"border: 0; width: 100%; height: 300px;\\\" allowfullscreen></iframe>\",\"height\":300,\"aspectRatio\":null}}" %}

### Detailed post concerning perspective

[https://css-tricks.com/almanac/properties/p/perspective/](https://css-tricks.com/almanac/properties/p/perspective/)

{% embed data="{\"url\":\"https://css-tricks.com/almanac/properties/p/perspective/\",\"type\":\"link\",\"title\":\"perspective \| CSS-Tricks\",\"description\":\"The perspective CSS property gives an element a 3D-space by affecting the distance between the Z plane and the user. The strength of the effect is\",\"icon\":{\"type\":\"icon\",\"url\":\"https://css-tricks.com/apple-touch-icon.png\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://cdn.css-tricks.com/wp-content/uploads/2014/03/css-tricks-star.png\",\"width\":512,\"height\":512,\"aspectRatio\":1}}" %}

