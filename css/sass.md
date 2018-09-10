---
description: Syntactically Awesome Style Sheets
---

# Sass

Natively, CSS is **verbose**, has **factorization limitations** and can be **hard to maintain**.

These issues are solved using **preprocessors like SASS**.

[http://sass-lang.com/](http://sass-lang.com/)

{% embed data="{\"url\":\"http://sass-lang.com/\",\"type\":\"link\",\"title\":\"Sass: Syntactically Awesome Style Sheets\",\"description\":\"Syntatically Awesome Style Sheets\",\"icon\":{\"type\":\"icon\",\"url\":\"http://sass-lang.com/favicon.ico\",\"aspectRatio\":0}}" %}

Preprocessors allow writing CSS in a language with the following features:

* Variables.
* Nesting.
* Mixins.
* Inheritance.

Preprocessors generate standard CSS.

```css
$wt-transition-duration: 0.5s;
$wt-user-list-background-color: blue;

.wt-user-list {

    background-color: $wt-user-list-background-color;

    >li {
        @include transition(transform @wt-transition-duration);
    }
        
}
```

Preprocessors can generate vendor prefixed CSS using modules like Bourbon.

​[http://bourbon.io/](http://bourbon.io/)

{% embed data="{\"url\":\"http://bourbon.io/\",\"type\":\"link\",\"title\":\"Bourbon - A Lightweight Sass Tool Set\",\"description\":\"Bourbon is a library of pure Sass mixins and functions that are designed to make you a more efficient style sheet author.\"}" %}



