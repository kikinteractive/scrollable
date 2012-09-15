scrollable.js - Seamless scrolling for mobile devices
=====================================================

Scrolling on mobile devices is inconsistent at best. scrollable.js provides a sane API that you're already familiar with to make scrolling easy. scrollable.js does not have any dependencies except for a custom version of [iScroll](http://cubiq.org/iscroll-4), which is privately included and not externalized at all.

scrollable.js also provides convenient bindings for ZeptoJS and jQuery to make the development process as seamless as possible.


Links
-----

[Download script (v1.0 minified)](http://code.kik.com/scrollable/1.0.min.js)

[View demo](http://code.kik.com/scrollable/demos/basic.html)


Usage with ZeptoJS or jQuery
----------------------------

### Make elements scrollable

```js
$(element).scrollable();
```


### Bind to scroll events

```js
$(element).on('scroll', function () {
	// fired on scroll
});
```


### Setting scroll offset

```js
$(element).scrollTop();    // retrieve Y offset
$(element).scrollTop(20);  // set Y offset

$(element).scrollLeft();   // retrive X offset
$(element).scrollLeft(20); // set X offset
```


### Manipulating scrollable region

When native scrolling is not available we must wrap your content and use [iScroll](http://cubiq.org/iscroll-4) to simulate scrolling.

Thus, to manipulate the scrollable region we must only add or remove content from the "scrollable node".

```js
$(element).scrollableNode()
          .append('<div>more stuff</div>');
```




Standalone Usage
----------------

scrollable.js has no external dependencies and will work perfectly fine as a standalone library.


### Make elements scrollable

```js
Scrollable(element);
```


### Bind to scroll events

```js
element.addEventListener('scroll', function () {
	// fired on scroll
}, false);
```


### Setting scroll offset

```js
element._scrollTop();    // retrieve Y offset
element._scrollTop(20);  // set Y offset

element._scrollLeft();   // retrive X offset
element._scrollLeft(20); // set X offset
```

Using the regular scrollTop/scrollLeft attributes will only work on newer mobile OS's. (iOS 5+ & Android 4+)


### Manipulating scrollable region

```js
Scrollable.node(element).innerHTML += '<div>more stuff</div>';
```