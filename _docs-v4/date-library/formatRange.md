---
title: formatRange
---

Formats a date range by intelligently inserting a dash between the two dates.

<div class='spec' markdown='1'>
$.fullCalendar.formatRange( *moment1*, *moment2*, *formatString* [, *separator*, *isRTL* ] ) -> String
</div>

`moment1` and `moment2` must be [Moment](moment) objects.

`formatString` is a [date formatting string](date-formatting-string) written as if it were for a single date, but FullCalendar will intelligently use it to format both dates with a dash in between.

Example:

```js
var moment1 = moment('2013-09-02');
var moment2 = moment('2013-09-09');
$.fullCalendar.formatRange(moment1, moment2, 'MMMM D YYYY');

=> "Sep 2 - 9 2013"
```
