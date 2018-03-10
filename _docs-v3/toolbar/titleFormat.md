---
title: titleFormat
---

Determines the text that will be displayed in the header's title.

<div class='spec' markdown='1'>
[format string](date-formatting-string), *default*:

```js
'MMMM YYYY'   // like 'September 2009', for month view
'MMM D YYYY'  // like 'Sep 13 2009', for week views
'MMMM D YYYY' // like 'September 8 2009', for day views
```
</div>

As noted above, each view has a specific default. Get fine-tuned control with [View-Specific Options](view-specific-options). A single string alone will set the value for all views.

The default values will change based on the current [locale](locale).
