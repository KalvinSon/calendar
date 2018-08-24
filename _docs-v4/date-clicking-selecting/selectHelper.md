---
title: selectHelper
---

Whether to draw a "placeholder" event while the user is dragging.

<div class='spec' markdown='1'>
Boolean, *default*: `false`
</div>

**This option only applies to the agenda views.**

A value of `true` will draw a "placeholder" event while the user is dragging (similar to what Google Calendar does for its week and day views). A value of `false` (the default) will draw the standard highlighting over each cell.

<div class='version-info' markdown='1'>
Versions 2.0.3 and prior allowed a function argument for generating custom elements.
For later versions, use [eventRender](eventRender) instead.
</div>
