---
title: eventResize
type: callback
---

Triggered when resizing stops and the event has changed in duration.

<div class='spec' markdown='1'>
function( *event*, *delta*, *revertFunc*, *jsEvent*, *ui*, *view* ) { }
</div>

`event` is an [Event Object](event-object) that hold the event's information (date, title, etc).

`delta` is a [Duration Object](moment-duration) that represents the amount of time the event's end was extended by. *Available in version 2.0.1 and later.*

`revertFunc` is a function that, if called, reverts the event's end date to the value before the drag. This is useful if an ajax call should fail.

`jsEvent` holds the native javascript event with low-level information such as mouse coordinates.

`ui` holds an empty object. Before version 2.1, the [jQuery UI object](http://jqueryui.com/demos/resizable/).

`view` holds the current [View Object](view-object).

Here is an example demonstrating most of these arguments:

```js
$('#calendar').fullCalendar({
  events: [
    // events here
  ],
  editable: true,
  eventResize: function(event, delta, revertFunc) {

    alert(event.title + " end is now " + event.end.format());

    if (!confirm("is this okay?")) {
      revertFunc();
    }

  }
});
```
