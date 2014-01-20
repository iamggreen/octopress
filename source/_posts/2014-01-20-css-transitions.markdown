---
layout: post
title: "CSS Transitions"
date: 2014-01-20 17:03:17 -0600
comments: true
categories: css
---

The CSS transition property allows the browser to listen to CSS property changes and instead of applying the change immediately, it animates(or transitions) the given property from the beginning state to the new state.  Like the animation property, this requires vendor prefixes and works with the most up to date browsers, including IE10+.

For the transition to work, you specify a css property for the browser to listen to.  Whenever that css property changes, the browser will apply the given transition.  An example of a transition property is below (Vendor prefixes have been removed for brevity): 

```
#ball {
    transition-property: left, top;
    transition-duration: 1s, 1s;
    transition-timing-function: ease-in, ease-in;
    transition-delay: 0, 0;
}
```

This can also be written shorthand as follows

```
#ball {    
    transition: left 1s ease-in 0, top 1s ease-in 0
}
```

The properties required for transition are as follows:

*  **transition-property** - Specifies the name of the CSS property to transition

---

*  **transition-duration** - Specifies the name of the CSS property to transition

---

*  **transition-timing-function** - Specifies the speed curve of the animation
   * Allowed values are ease(default), linear, ease-in, ease-out, ease-in-out, cubic-bezier

---

*  **transition-delay** - Specifies a delay before the animation will start

---

The shorthand version is: 

```
transition: transition transition-duration transition-timing-function transition-delay
```

See [My JSFiddle for an example.](http://jsfiddle.net/iamggreen/UAyU6/1)