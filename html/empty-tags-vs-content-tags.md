# Empty Tags vs Content Tags

Some tags like `div`, `span` and `p` need content.

{% hint style="warning" %}
Do not mix text with tags inside a content tag.

Otherwise, formatting and dynamic content modification can get complicated.

```markup
<!-- Dirty! -->
<div>
    Hello
    <span>Mr Foo</span>
</div>


<!-- Clean. -->
<div>
    <span>Hello</span>
    <span>Mr Foo</span>
</div>
```
{% endhint %}

With HTML5, empty tags don't need to be closed.

The following examples are equivalent:

```markup
<!-- Auto-closing tag. -->
<input type="text"/>

<!-- Implicit auto-closing tag. -->
<input type="text">
```

Closing empty tags might seem cleaner but it is better to leave them open.

Auto-closing tags might be ignored by some browsers and can cause trouble.

