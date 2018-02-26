---
title: height
---

Sets the height of the entire calendar, including header and footer.

<div class='spec' markdown='1'>
Integer, Function, `"parent"`, `"auto"`
</div>

By default, this option is unset and the calendar's height is calculated by [aspectRatio](aspectRatio).

If an integer is specified, the height of the calendar will be guaranteed to be that exact pixel height.
If the contents will not fit within the height, scrollbars will appear (new in version 2.1.0).

If a function is specified, this function will be called every time a height update is requested. This function should return a pixel value.

If `"parent"` is specified, the height of the calendar will match the height of its parent container element. [See an example](full-height-demo).

If `"auto"` is specified, the view's contents will assume a natural height and no scrollbars will be used. (new in version 2.1.0).

Example usage of `height`:

```js
$('#calendar').fullCalendar({
  height: 650
});
```

## Setter

You can dynamically set a calendar's height after initialization:

```js
$('#calendar').fullCalendar('option', 'height', 700);
```
