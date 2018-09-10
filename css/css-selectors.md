# CSS Selectors

## CSS selector examples

```css
/* Tag. */
p { ... }

/* Id. */
#wt-wish-list { ... }

/* Class. */
.wt-wish { ... }

/* Multiple criteria: Tag with a specific class. */
p.wt-bold { ... }

/* Factorization: Apply same style to multiple selectors. */
p, #wt-wish-list, .wt-wish { ... }

/* Child element: Apply style to every button which is contained in an element with a "wt-button-container" class. */
.wt-button-container button { ... }

/* Direct child element. */
.wt-button-container > button { ... }

/* Pseudo-classes. */
.wt-button-container:hover { ... }

.wt-button-container:first-child { ... }
```

{% hint style="success" %}
Prefer using class-based selectors.
{% endhint %}

{% hint style="info" %}
To avoid collisions and improve readability, add a **prefix** to your CSS classes.

_Especially if you are not using a framework and that your CSS is global \(and not specific to some component\)._ 
{% endhint %}

## Pseudo-classes

Pseudo-classes allow you to **customize the CSS depending on the context or state of the element** _\(e.g.: is it the first element of a list, is it a checked checkbox etc...\)_.

[https://www.w3.org/wiki/CSS/Selectors\#Pseudo-classes](https://www.w3.org/wiki/CSS/Selectors#Pseudo-classes)

{% embed data="{\"url\":\"https://www.w3.org/wiki/CSS/Selectors\#Pseudo-classes\",\"type\":\"link\",\"title\":\"CSS/Selectors - W3C Wiki\",\"icon\":{\"type\":\"icon\",\"url\":\"https://www.w3.org/favicon.ico\",\"aspectRatio\":0}}" %}



