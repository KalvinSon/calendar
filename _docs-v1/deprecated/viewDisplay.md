---
title: viewDisplay
since_version: 1.3
---

Triggered when the calendar loads and every time a different date-range is displayed.

<div class='removed-notice'>
This option has been deprecated in favor of the <a href='viewRender'>viewRender</a> callback.
</div>


<div class='spec' markdown='1'>
function( *view* ) { }
</div>

The calendar's date-range changes whenever the user switches to a new view (for example, if they switch from "month" to "agendaWeek") or when they click the prev/next buttons.

`view` is the current [View Object](view-object).

Within the callback function, `this` will be set to the calendar's main element.

Example usage of viewDisplay:

```js
$('#calendar').fullCalendar({
  viewDisplay: function(view) {
    alert('The new title of the view is ' + view.title);
  }
});
```

<div class='version-info' markdown='1'>
In versions 1.0 through 1.2.1, this option was known as *monthDisplay*.
</div>
