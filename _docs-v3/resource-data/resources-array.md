---
title: resources (as an array)
---

Tells the calendar to display resources from an array input.

```js
$('#calendar').fullCalendar({
  resources: [
    {
      id: 'a',
      title: 'Room A'
    },
    {
      id: 'b',
      title: 'Room B'
    }
  ]
});
```

The `id` property is the most important because it allows [associating events with resources](resources-and-events). See the [Resource Object](resource-object) spec for a full list of fields.
