---
layout: post
title: "CSS Declaration Precedence"
date: 2014-01-15 21:48:54 -0600
comments: true
categories: html
---

The W3 Specifications on CSS 2.1 say what the CSS Declaration Precedence order but I found it harder to track down what each type of declaration actually is.  This is the definitions in order.

**CSS Declaration Precedence Order ** (#5 has the highest precedence)

1.  **User Agent Declarations**

	These are the default declarations added by the browser

2.  **User Normal Declarations**

	These are the declarations specified by the user in the browser that override the user agent declarations.  Usually in the browser settings/options tabs.

3.  **Author Normal Declarations**

	These are declarations used by a particular web page.

4.  **Author Important Declarations**
	Same as Author Normal declarations but with !important added

5.  **User Important Declarations**
	Same as User Normal declarations but with !important added
	

References

[What is the difference between a user and an author style sheet?](http://webdesign.about.com/od/css/f/blcssfaqdifusau.htm)

[CSS Cascading order](http://www.w3.org/TR/CSS21/cascade.html#cascading-order)