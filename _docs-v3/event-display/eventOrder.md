---
title: eventOrder
since_version: 2.4.0
---

Determines the vertical ordering events that have the same times.

<div class='spec' markdown='1'>
String / Array / Function, *default*: `"title"`
</div>

By default, FullCalendar decides that events with longer durations and earlier start times are sorted above other events. However, events often have the same exact start time and duration, which is especially true for all-day events. By default, when this happens, events are sorted alphabetically by title. `eventOrder` provides the ability to override this behavior.

This setting accepts a few different arguments:

- a name of an [Event Object](event-object) property, like `"title"`.
  This can be the name of a non-standard field.
  Sorting will happen in ascending order.
  If prefixed with a minus sign like `"-title"`, sorting will happen in descending order.

- a comma-separated string of property names, like `"title,propA,-propB"`

- a *function* that accepts two arguments and returns `-1` or `1`, similar to
  [sort's compare function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort).

- an array of property names and functions
  like `[ "title", "-propA", myFunc ]`.
