# Animations

CSS animations describe a **chain of transition steps**.

Each step is called a **keyframe**.

```css
@keyframes demo-animation {

    0% {
        background-color: #ffffff;
        color: #000000;
        width: 73px;
    }

    33% {
        background-color: rgb(63,81,181);
        color: #ffffff;
        width: 73px;
    }

    66% {
        background-color: rgb(63,81,181);
        color: #ffffff;
        width: 173px;
    }

    100% {
        background-color: #ffffff;
        color: #000000;
        width: 173px;
    }

}

.wt-demo-animation {
  
    border-style: solid;
    border-width: 1px;
    text-align: center;
    width: 73px;
    margin: auto;
    padding: 10px;
  
}

.wt-demo-animation:hover {

    animation-name: demo-animation;
    animation-direction: alternate;
    animation-duration: 2s;
    animation-iteration-count: infinite;
    animation-timing-function: linear;

}
```

[https://codepen.io/younes-jaaidi/pen/eLVybG](https://codepen.io/younes-jaaidi/pen/eLVybG)

{% embed data="{\"url\":\"https://codepen.io/younes-jaaidi/pen/eLVybG\",\"type\":\"rich\",\"title\":\"web-dev-css-animation\",\"description\":\"...\",\"icon\":{\"type\":\"icon\",\"url\":\"https://codepen.io/favicons/favicon-192x192.png\",\"width\":192,\"height\":192,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://s3-us-west-2.amazonaws.com/i.cdpn.io/2355348.eLVybG.small.28fe2586-fed6-4bb4-84e4-cb7845f75acd.png\",\"width\":384,\"height\":225,\"aspectRatio\":0.5859375},\"embed\":{\"type\":\"app\",\"url\":\"https://codepen.io/younes-jaaidi/embed/preview/eLVybG?height=300&slug-hash=eLVybG&default-tabs=css,result&host=https://codepen.io&embed-version=2\",\"html\":\"<iframe src=\\\"https://codepen.io/younes-jaaidi/embed/preview/eLVybG?height=300&amp;slug-hash=eLVybG&amp;default-tabs=css,result&amp;host=https://codepen.io&amp;embed-version=2\\\" style=\\\"border: 0; width: 100%; height: 300px;\\\" allowfullscreen></iframe>\",\"height\":300,\"aspectRatio\":null}}" %}

## Animate.css

The **animate.css** module implements lots of interesting animations.

[https://daneden.github.io/animate.css/](https://daneden.github.io/animate.css/)

{% embed data="{\"url\":\"https://daneden.github.io/animate.css/\",\"type\":\"link\",\"title\":\"Animate.css\"}" %}

[  
](https://daneden.github.io/animate.css/
)

