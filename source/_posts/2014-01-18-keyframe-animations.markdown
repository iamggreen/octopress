---
layout: post
title: "Keyframe Animations"
date: 2014-01-18 11:27:15 -0600
comments: true
categories: css
---

CSS3 defines a property called keyframes in order to allow animation to be done via CSS.  While this works in most up-to-date browsers (Chrome, IE9+, Mozilla, Opera) they all require vendor prefixes to work as the standard properties do not currently work on any browser.  All animation properties as well as the @keyframe declaration must have a vendor prefix to work.  The vendor prefixes have been left of in this article for brevity.

To start, we need to create a keyframe animation.  It looks something like this.

```
@keyframes sunrise {
        0% {
                bottom: 0;
                left: 340px;
                background: #f00;
        }
        
        33% {
                bottom: 340px;
                left: 340px;
                background: #ffd630;
        }

        66% {
                bottom: 340px;
                left: 40px;
                background: #ffd630;
        }

        100% {
                bottom: 0;
                left: 40px;
                background: #f00;
        }
}
```

This is pretty self explanatory.  It creates an animation named "sunrise".  The percentages define where the transitions need to be at the time interval for that percent.  0% and 100% are where the transition starts and ends. Also, to/from property names can be used interchangeably with 0%/100%, respectively.

Now we need to assign that keyframe animation to a given element of set of elements based on a css selector.  It looks like this.

```
#sun.animate {
        animation-name: sunrise;
        animation-duration: 10s;
        animation-timing-function: ease;
        animation-iteration-count: 1;
        animation-direction: normal;
        animation-delay: 0;
        animation-play-state: running;
        animation-fill-mode: forwards;
}
```

The properties are:

* **animation-name**  - Specifies the name of the keyframe you want to bind to the selector

---

* **animation-duration** - Specifies how many seconds or milliseconds an animation takes to complete

---

* **animation-timing-function** - Specifies the speed curve of the animation
	* Allowed values are ease(default), linear, ease-in, ease-out, ease-in-out, cubic-bezier(Dont ask, no clue?!?!)

---	

* **animation-iteration-count** - Specifies how many times an animation should be played

---

* **animation-direction** Specifies whether or not the animation should play in reverse on alternate cycles
	* Allowed values are normal(default), reverse, alternate, alternate-reverse

---
	
* **animation-delay** - Specifies a delay before the animation will start

---

* **animation-play-state** Specifies whether the animation is running or paused
	* Allowed values are running(default), paused

---
	
* **animation-fill-mode** Specifies what values are applied by the animation outside the time it is executing
	* Allowed values are none(default), forwards, backwards, both
	
--- 

The shorthand version for the animation property is: 

```
animation: animation-name animation-duration animation-timing-function animation-delay animation-play-state animation-fill-direction;
```

And that's most of what you need to start playing with animations in CSS.  Some of the pages I put together for my learning are below.  Have fun!


[KeyFrameHelloWorld on GitHub](https://github.com/iamggreen/KeyFramesHelloWorld)

[Keyframe Orbits JSFiddle](http://jsfiddle.net/iamggreen/e7YPB/1/)