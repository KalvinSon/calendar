---
title: addResource
type: method
---

Allows programmatic rendering of a new resource on the calendar after the initial set of resources has already been displayed.

<div class='spec' markdown='1'>
.fullCalendar( 'addResource', resource, scroll )
</div>

The `resource` argument should be a [Resource Object](resource-object). Example:

```js
$('#calendar').fullCalendar('addResource', {
  id: 'e',
  title: 'Room E'
});
```

If you would like the new resource to be a child of an existing resource, make sure to set its `parentId`.

If the `scroll` argument is `true`, the current view will scroll to the newly added resource to ensure it is visible.

[View a demo](addResource-demo) that utilizes addResource.
