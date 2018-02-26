---
title: eventResizeStart
type: callback
---

Triggered when event resizing begins.

<div class='spec' markdown='1'>
function( *event*, *jsEvent*, *ui*, *view* ) { }
</div>

`event` is an [Event Object](event-object) that hold the event's information (date, title, etc).

`jsEvent` holds the native JavaScript event with low-level information such as mouse coordinates.

`ui` holds an empty object. Before version 2.1, the [jQuery UI object](http://jqueryui.com/demos/resizable/).

`view` holds the current [View Object](view-object).
