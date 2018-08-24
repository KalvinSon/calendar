---
title: selectAllow
since_version: 3.0
---

Exact programmatic control over where the user can select.

<div class='spec' markdown='1'>
function(selectInfo)
</div>

This callback will be called for every new potential selection as the user is dragging.

The callback function will receive information about where the user is attempting to select (`selectInfo`) and must return either `true` or `false`.

The `selectInfo` object will have the following properties:

- `start` (a [Moment](moment))
- `end` exclusive end date/time (a [Moment](moment))
- `resourceId` if you are using a [Resource View](scheduler)
