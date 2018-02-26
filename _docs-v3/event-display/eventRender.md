---
title: eventRender
type: callback
---

Triggered while an event is being rendered. A hook for modifying its DOM.

<div class='spec' markdown='1'>
function( *event*, *element*, *view* ) { }
</div>

`event` is the [Event Object](event-object) that is attempting to be rendered.

`element` is a newly created jQuery element that will be used for rendering. It has already been populated with the correct time/title text.

The `eventRender` callback function can modify `element`. For example, it can change its appearance via jQuery's `.css()`.

The function can also return a brand new element that will be used for rendering instead. For all-day [background events](background-events), you must be sure to return a `<td>`.

The function can also return `false` to completely cancel the rendering of the event.

`eventRender` is a great way to attach other jQuery plugins to event elements, such as a [qTip](http://craigsworks.com/projects/qtip/) tooltip effect:

```js
$('#calendar').fullCalendar({
  events: [
    {
      title: 'My Event',
      start: '2010-01-01',
      description: 'This is a cool event'
    }
    // more events here
  ],
  eventRender: function(event, element) {
    element.qtip({
      content: event.description
    });
  }
});
```

Note that `description` is a non-standard Event Object field, which is allowed.
