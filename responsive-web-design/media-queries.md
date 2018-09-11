# Media Queries

## Media width

Media queries allow **CSS modification depending on the screen's size**.

```markup
<button
        class="wt-hide-gt-sm"
        data-role="wt-menu-button">Menu</button>

<div class="wt-show-gt-sm">
    <button>Action 1</button>
    <button>Action 2</button>
    <button>Action 3</button>
    <button>Action 4</button>
</div>
```

```css
@media (max-width: 599px) {
    .wt-show-gt-sm {
        display: none;
    }
}

@media (min-width: 600px) {
    .wt-hide-gt-sm {
        display: none;
    }
}
```

[https://codepen.io/younes-jaaidi/pen/LJdQQv](https://codepen.io/younes-jaaidi/pen/LJdQQv)

{% embed data="{\"url\":\"https://codepen.io/younes-jaaidi/pen/LJdQQv\",\"type\":\"rich\",\"title\":\"web-dev-responsive\",\"description\":\"...\",\"icon\":{\"type\":\"icon\",\"url\":\"https://codepen.io/favicons/favicon-192x192.png\",\"width\":192,\"height\":192,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://s3-us-west-2.amazonaws.com/m.cdpn.io/screenshot-coming-soon-small.png\",\"width\":400,\"height\":225,\"aspectRatio\":0.5625},\"embed\":{\"type\":\"app\",\"url\":\"https://codepen.io/younes-jaaidi/embed/preview/LJdQQv?height=300&slug-hash=LJdQQv&default-tabs=html,result&host=https://codepen.io&embed-version=2\",\"html\":\"<iframe src=\\\"https://codepen.io/younes-jaaidi/embed/preview/LJdQQv?height=300&amp;slug-hash=LJdQQv&amp;default-tabs=html,result&amp;host=https://codepen.io&amp;embed-version=2\\\" style=\\\"border: 0; width: 100%; height: 300px;\\\" allowfullscreen></iframe>\",\"height\":300,\"aspectRatio\":null}}" %}

## Media orientation

It is also possible to modify CSS depending on the **device's orientation**.

```css
@media (orientation: landscape) {
    ...
}
```



