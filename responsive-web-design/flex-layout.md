# Flex Layout

Flexbox layout dynamically modifies its child elements sizes to fill out the available area.

```markup
<div class="wt-flexbox-container">
    <div>Item 1</div>
    <div>Item 2</div>
    <div>Item 3</div>
</div>
```

```css
.wt-flexbox-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
}

.wt-flexbox-container>div {

    border-style: solid;
    border-width: 1px;
    padding: 10px;
    text-align: center;

    flex: 1;
    min-width: 200px;

}
```

[https://codepen.io/younes-jaaidi/pen/KxooqG](https://codepen.io/younes-jaaidi/pen/KxooqG)

{% embed data="{\"url\":\"https://codepen.io/younes-jaaidi/pen/KxooqG\",\"type\":\"rich\",\"title\":\"web-dev-flexbox\",\"description\":\"...\",\"icon\":{\"type\":\"icon\",\"url\":\"https://codepen.io/favicons/favicon-192x192.png\",\"width\":192,\"height\":192,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://s3-us-west-2.amazonaws.com/m.cdpn.io/screenshot-coming-soon-small.png\",\"width\":400,\"height\":225,\"aspectRatio\":0.5625},\"embed\":{\"type\":\"app\",\"url\":\"https://codepen.io/younes-jaaidi/embed/preview/KxooqG?height=300&slug-hash=KxooqG&default-tabs=css,result&host=https://codepen.io&embed-version=2\",\"html\":\"<iframe src=\\\"https://codepen.io/younes-jaaidi/embed/preview/KxooqG?height=300&amp;slug-hash=KxooqG&amp;default-tabs=css,result&amp;host=https://codepen.io&amp;embed-version=2\\\" style=\\\"border: 0; width: 100%; height: 300px;\\\" allowfullscreen></iframe>\",\"height\":300,\"aspectRatio\":null}}" %}

## More Links

[https://css-tricks.com/snippets/css/a-guide-to-flexbox/](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

{% embed data="{\"url\":\"https://css-tricks.com/snippets/css/a-guide-to-flexbox/\",\"type\":\"link\",\"title\":\"A Complete Guide to Flexbox \| CSS-Tricks\",\"description\":\"Our comprehensive guide to CSS flexbox layout. This complete guide explains everything about flexbox, focusing on all the differnet possible properties for the parent element \(the flex container\) and the child elements \(the flex items\). It also includes history, demos, patterns, and a browser support chart.\",\"icon\":{\"type\":\"icon\",\"url\":\"https://cdn.css-tricks.com/apple-touch-icon.png\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://cdn.css-tricks.com/wp-content/uploads/2011/08/flexbox.png\",\"width\":659,\"height\":281,\"aspectRatio\":0.4264036418816389}}" %}

