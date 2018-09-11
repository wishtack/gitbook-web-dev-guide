# Grid Layout

CSS Grid Layout allows item positioning in a grid based on columns and rows without having to struggle with floats, positioning or bootstrap's css classes.

```markup
<div class="wt-grid-container">
    <div class="wt-item-green">GREEN</div>
    <div class="wt-item-orange">ORANGE</div>
    <div class="wt-item-red">RED</div>
    <div class="wt-item-blue">BLUE</div>
</div>
```

```css
.wt-grid-container {
    display: grid;
    grid-template-columns: 1fr 1fr 2fr;
    grid-template-rows: 1fr 1fr 1fr;
}

.wt-item-green {
    background-color: green;
    grid-area: 1 / 1 / 1 / 3;
}

.wt-item-blue {
    background-color: blue;
    grid-column: 3;
    grid-row: 1;
}

.wt-item-orange {
    background-color: orange;
    grid-column: 1 / 2;
    grid-row: 2 / 4;
}

.wt-item-red {
    background-color: red;
    grid-area: 2 / 2 / 4 / 4;
}
```

[https://codepen.io/younes-jaaidi/pen/RYMQqW](https://codepen.io/younes-jaaidi/pen/RYMQqW)

{% embed data="{\"url\":\"https://codepen.io/younes-jaaidi/pen/RYMQqW\",\"type\":\"rich\",\"title\":\"web-dev-grid-layout\",\"description\":\"...\",\"icon\":{\"type\":\"icon\",\"url\":\"https://codepen.io/favicons/favicon-192x192.png\",\"width\":192,\"height\":192,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://s3-us-west-2.amazonaws.com/i.cdpn.io/2355348.RYMQqW.small.98354186-9ba8-4e43-89ce-7432f4d04b84.png\",\"width\":384,\"height\":225,\"aspectRatio\":0.5859375},\"embed\":{\"type\":\"app\",\"url\":\"https://codepen.io/younes-jaaidi/embed/preview/RYMQqW?height=300&slug-hash=RYMQqW&default-tabs=css,result&host=https://codepen.io&embed-version=2\",\"html\":\"<iframe src=\\\"https://codepen.io/younes-jaaidi/embed/preview/RYMQqW?height=300&amp;slug-hash=RYMQqW&amp;default-tabs=css,result&amp;host=https://codepen.io&amp;embed-version=2\\\" style=\\\"border: 0; width: 100%; height: 300px;\\\" allowfullscreen></iframe>\",\"height\":300,\"aspectRatio\":null}}" %}

[https://learncssgrid.com/](https://learncssgrid.com/)

{% embed data="{\"url\":\"https://learncssgrid.com/\",\"type\":\"link\",\"title\":\"Learn CSS Grid - A Guide to Learning CSS Grid\",\"description\":\"A comprehensive guide to help you understand and learn CSS Grid Layout, by Jonathan Suh.\",\"icon\":{\"type\":\"icon\",\"url\":\"https://learncssgrid.com/favicon.ico\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"http://learncssgrid.com/screenshot.png\",\"width\":1201,\"height\":537,\"aspectRatio\":0.44712739383846795}}" %}

