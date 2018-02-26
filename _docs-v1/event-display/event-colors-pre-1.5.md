---
title: Event Coloring prior to version 1.5
type: guide
---

Prior to v1.5, you must modify the default color that affects all events by adding some css in the following form:

```css
.fc-event,
.fc-agenda .fc-event-time,
.fc-event a {
  background-color: black; /* background color */
  border-color: black;     /* border color */
  color: red;              /* text color */
  }
```

You can also change the color for certain events by using the `className` property of each [Event Object](event-object). Here is an example of the CSS you would write if your `className` was "holiday":

```css
.holiday,
.fc-agenda .holiday .fc-event-time,
.holiday a {
  background-color: green; /* background color */
  border-color: green;     /* border color */
  color: yellow;           /* text color */
  }
```

If you are using the "default" and "className" techniques together, make sure the CSS for the default technique comes first.

<p class='abstract' style='display:none'>
How to change colors of events through CSS.
</p>

<div class='version-info' markdown='1'>
Versions prior to 1.3 had different ways of setting colors through CSS.
Check your version's *fullcalendar.css* for an example.
</div>
