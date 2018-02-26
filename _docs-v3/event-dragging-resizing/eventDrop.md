---
title: eventDrop
type: callback
---

Triggered when dragging stops and the event has moved to a *different* day/time.

<div class='spec' markdown='1'>
function( *event*, *delta*, *revertFunc*, *jsEvent*, *ui*, *view* ) { }
</div>

`event` is an [Event Object](event-object) that hold the event's information (date, title, etc). Call `hasTime` on the event's `start`/`end` to see if it has been dropped in a timed or all-day area ([more info](moment#ambiguously-timed)).

`delta` is a [Duration Object](moment-duration) that represents the amount of time the event was moved by. *Available in version 2.0.1 and later.*

`revertFunc` is a function that, if called, reverts the event's start/end date to the values before the drag. This is useful if an ajax call should fail.

`jsEvent` holds the native JavaScript event with low-level information such as mouse coordinates.

`ui` holds an empty object. Before version 2.1, the [jQuery UI object](http://jqueryui.com/demos/draggable/).

`view` holds the current [View Object](view-object).

eventDrop *does not* get called when an external event lands on the calendar. [eventReceive](eventReceive) is called instead.

Here is an example demonstrating most of these arguments:

```js
$('#calendar').fullCalendar({
  events: [
    // events here
  ],
  editable: true,
  eventDrop: function(event, delta, revertFunc) {

    alert(event.title + " was dropped on " + event.start.format());

    if (!confirm("Are you sure about this change?")) {
      revertFunc();
    }

  }
});
```

## Resources

When an event has been newly dropped on a resource, the [Event Object's](event-object) `resourceId` will be updated to reflect.
