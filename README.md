
# DirectionAwareHoverEffect

How to create a direction-aware hover effect using CSS3 and jQuery. The idea is to slide in an overlay from the direction we are moving with the mouse.

[article on Codrops](http://tympanus.net/codrops/?p=8328)

[demo](http://tympanus.net/TipsTricks/DirectionAwareHoverEffect/)

### How to use

```js
$('#da-thumbs > li').hoverdir();
// or with options
$('#da-thumbs > li').hoverdir({hoverDelay: 75, hoverElem: '.elem'});
```
### Default options

```js
defaults: {
    speed: 300, // Times in ms
    easing: 'ease',
    hoverDelay: 0, // Times in ms
    inverse: false,
    hoverElem: 'div'
}
```

### Method

**show**

Show the hover element, after `show` method is triggered, hover don't show or hide on `mouseenter` and `mouseleave`.
You have to use `hide` method to bind `mouseenter` and `mouseleave`.
```js
$('#da-thumbs > li').hoverdir('show'); // Default value top
// or with a specific direction
$('#da-thumbs > li').hoverdir('show','bottom'); // Possible value top, right, bottom, left
```

**hide**

Hide the hover element and bind `mouseenter` and `mouseleave`.
```js
$('#da-thumbs > li').hoverdir('hide'); // Default value bottom
// or with a specific direction
$('#da-thumbs > li').hoverdir('hide','top'); // Possible value top, right, bottom, left
```

**setOptions**

Allows you to change the options while the plugin is already running
```js
$('#da-thumbs > li').hoverdir('setOptions', options);
```

**destroy**

Unbind the plugin
```js
$('#da-thumbs > li').hoverdir('destroy');
```

**rebuild**

Bind the plugin
```js
$('#da-thumbs > li').hoverdir('rebuild');
// or with options
$('#da-thumbs > li').hoverdir('rebuild', options);
```

Licensed under the MIT License