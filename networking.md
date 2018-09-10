# Networking

**Most data** you application will display to your users and let them interact with, **will come from remote network sources**.

Most of these sources will be [ReSTful APIs](https://blog.wishtack.com/rest-apis-best-practices-and-security/) or [GraphQL APIs](https://graphql.org).

[https://blog.wishtack.com/rest-apis-best-practices-and-security/](https://blog.wishtack.com/rest-apis-best-practices-and-security/)

{% embed data="{\"url\":\"https://blog.wishtack.com/rest-apis-best-practices-and-security/\",\"type\":\"link\",\"title\":\"ReST APIs \| Best Practices & Security\",\"description\":\"A white paper covering all the best practices and security concerns about ReST APIs.\",\"icon\":{\"type\":\"icon\",\"url\":\"https://wishtackblog.files.wordpress.com/2017/03/cropped-wishtack\_logo\_1024x1024.png?w=192\",\"width\":192,\"height\":192,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://wishtackblog.files.wordpress.com/2017/03/smurf-api.png?w=640\",\"width\":298,\"height\":314,\"aspectRatio\":1.0536912751677852}}" %}

[https://graphql.org](https://graphql.org)

{% embed data="{\"url\":\"https://graphql.org\",\"type\":\"link\",\"title\":\"GraphQL: A query language for APIs.\",\"description\":\"GraphQL provides a complete description of the data in your API, gives clients the power to ask for exactly what they need and nothing more, makes it easier to evolve APIs over time, and enables powerful developer tools.\",\"icon\":{\"type\":\"icon\",\"url\":\"https://graphql.org/img/favicon.png\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://graphql.org/img/og\_image.png\",\"width\":1200,\"height\":630,\"aspectRatio\":0.525}}" %}

{% hint style="warning" %}
Luckily, thanks to the `fetch` web API and without any external library, we will not need to use the old fashioned `XMLHttpRequest` object.

```javascript
const xmlHttpRequest = new XMLHttpRequest();

xmlHttpRequest.onreadystatechange = () => {
    if (xmlHttpRequest.readyState === 4 /* request is complete */
        && xmlHttpRequest.status === 200) {
        document.querySelector('.wt-wish-list').innerHTML = xmlHttpRequest.responseText;
    }
};

xmlHttpRequest.open('GET', '/users/123456/wishes/', true /* async */);

xmlHttpRequest.send();
```
{% endhint %}





