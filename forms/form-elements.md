# Form elements

## `<fieldset>`, `<legend>` and `<label>`

```markup
<form>
    <fieldset>
      
        <legend>Book</legend>

        <div>
            <label for="title">Title</label>
            <input id="title" placeholder="title"     type="text">
        </div>

        <div>
            <label for="author-name">Author</label>
            <input id="author-name" placeholder="author"     type="text">
        </div>
      
    </fieldset>
</form>
```

[https://codepen.io/younes-jaaidi/pen/RYQMEM](https://codepen.io/younes-jaaidi/pen/RYQMEM)

{% embed data="{\"url\":\"https://codepen.io/younes-jaaidi/pen/RYQMEM\",\"type\":\"rich\",\"title\":\"web-dev-form\",\"description\":\"...\",\"icon\":{\"type\":\"icon\",\"url\":\"https://codepen.io/favicons/favicon-192x192.png\",\"width\":192,\"height\":192,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://s3-us-west-2.amazonaws.com/m.cdpn.io/screenshot-coming-soon-small.png\",\"width\":400,\"height\":225,\"aspectRatio\":0.5625},\"embed\":{\"type\":\"app\",\"url\":\"https://codepen.io/younes-jaaidi/embed/preview/RYQMEM?height=300&slug-hash=RYQMEM&default-tabs=html,result&host=https://codepen.io&embed-version=2\",\"html\":\"<iframe src=\\\"https://codepen.io/younes-jaaidi/embed/preview/RYQMEM?height=300&amp;slug-hash=RYQMEM&amp;default-tabs=html,result&amp;host=https://codepen.io&amp;embed-version=2\\\" style=\\\"border: 0; width: 100%; height: 300px;\\\" allowfullscreen></iframe>\",\"height\":300,\"aspectRatio\":null}}" %}

## `<datalist>`

```markup
<form>

    <datalist id="dataList">
        <option value="foo@bar.com" label="John Doe"></option>
        <option value="contact@wishtack.com" label="Wishtack"></option>
    </datalist>

    <input list="dataList" type="email">

</form>
```

[https://codepen.io/younes-jaaidi/pen/RYQMvM](https://codepen.io/younes-jaaidi/pen/RYQMvM)

{% embed data="{\"url\":\"https://codepen.io/younes-jaaidi/pen/RYQMvM\",\"type\":\"rich\",\"title\":\"web-dev-form-datalist\",\"description\":\"...\",\"icon\":{\"type\":\"icon\",\"url\":\"https://codepen.io/favicons/favicon-192x192.png\",\"width\":192,\"height\":192,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://s3-us-west-2.amazonaws.com/m.cdpn.io/screenshot-coming-soon-small.png\",\"width\":400,\"height\":225,\"aspectRatio\":0.5625},\"embed\":{\"type\":\"app\",\"url\":\"https://codepen.io/younes-jaaidi/embed/preview/RYQMvM?height=300&slug-hash=RYQMvM&default-tabs=html,result&host=https://codepen.io&embed-version=2\",\"html\":\"<iframe src=\\\"https://codepen.io/younes-jaaidi/embed/preview/RYQMvM?height=300&amp;slug-hash=RYQMvM&amp;default-tabs=html,result&amp;host=https://codepen.io&amp;embed-version=2\\\" style=\\\"border: 0; width: 100%; height: 300px;\\\" allowfullscreen></iframe>\",\"height\":300,\"aspectRatio\":null}}" %}

