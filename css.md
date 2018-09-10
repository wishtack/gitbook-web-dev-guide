# CSS

## Cascading Style Sheets, Why?

**HTML** has been designed to describe a **document's content but not it's display**.

{% hint style="danger" %}
Formatting tags \(`<b>`, `<br>`, `<i>`\) should not be used. 
{% endhint %}

{% hint style="success" %}
CSS should be used instead.

**Separation of Concerns:** CSS allows separation of content and design.
{% endhint %}

## CSS is quite powerful

[https://codepen.io/davidkpiano/pen/kkpGWj](https://codepen.io/davidkpiano/pen/kkpGWj)

{% embed data="{\"url\":\"https://codepen.io/davidkpiano/pen/kkpGWj\",\"type\":\"rich\",\"title\":\"Meshi the CSS Dog\",\"description\":\"A CSS-only animated dog based on a \[Dribbble by Gal Shir\]\(https://dribbble.com/shots/3011370-This-is-my-dog-Meshi\).  Works in all modern browsers....\",\"icon\":{\"type\":\"icon\",\"url\":\"https://codepen.io/favicons/favicon-192x192.png\",\"width\":192,\"height\":192,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://s3-us-west-2.amazonaws.com/i.cdpn.io/181794.kkpGWj.small.6ba007d3-9d54-4de5-ac1c-655016fe2a69.png\",\"width\":384,\"height\":225,\"aspectRatio\":0.5859375},\"embed\":{\"type\":\"app\",\"url\":\"https://codepen.io/davidkpiano/embed/preview/kkpGWj?height=300&slug-hash=kkpGWj&default-tabs=css,result&host=https://codepen.io&embed-version=2\",\"html\":\"<iframe src=\\\"https://codepen.io/davidkpiano/embed/preview/kkpGWj?height=300&amp;slug-hash=kkpGWj&amp;default-tabs=css,result&amp;host=https://codepen.io&amp;embed-version=2\\\" style=\\\"border: 0; width: 100%; height: 300px;\\\" allowfullscreen></iframe>\",\"height\":300,\"aspectRatio\":null}}" %}

## How it works

### 1. Writing CSS

CSS syntax is basically composed of **selectors**, **properties** and **values**.

```css
selector {

    /* Comment your CSS! */
    property: value;
    ...

}
```

* The **selector**: allows you to select which elements in the page are concerned by this styling.
* The **property**: is the the styling property you want to control.
* The **value**: is the value you want to set on the property.

#### Example

```css
p {
    color: red;
    text-align: center;
}
```

### 2. Loading CSS

Except if you are using a framework, CSS is generally loaded using the HTML `<link>` tag.

```markup
<head>
    <link href="/assets/style.css" rel="stylesheet" type="text/css">
</head>
```



