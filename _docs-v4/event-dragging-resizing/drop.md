---
title: drop
type: callback
---

Called when a valid external jQuery UI draggable has been dropped onto the calendar.

<div class='spec' markdown='1'>
function( *date*, *jsEvent*, *ui*, *resourceId* ) { }
</div>

`date` holds the [Moment](moment) of where the draggable was dropped. It will either have a time, or be [ambiguously-timed](moment#ambiguously-timed), depending on whether it was dropped on an all-day area or not.

`jsEvent` holds the primitive JavaScript event, with information like mouse coordinates.

`ui` holds the jQuery UI information.

`resourceId` will be populate if dropped on a [Scheduler](scheduler) resource.

`this` holds the DOM element that has been dropped.

To see this callback function in action, view the [droppable](droppable) article or see [this live demo](external-dragging-demo).
