---
title: Date Formatting Strings
---

Date formatting strings are used throughout the API and determine how a given [Moment](moment) object is rendered to a string.

FullCalendar leverages MomentJS for most date-related operations including formatting dates:

> **[See MomentJS's formatting characters](http://momentjs.com/docs/#/displaying/format/)**

However, FullCalendar has extended Moment's functionality a bit by adding additional formatting characters:

<table>
<tr><th>T</th><td>renders "A" or "P" (one-letter, uppercase, for AM or PM)</td></tr>
<tr><th>t</th><td>renders "a" or "p" (one-letter, lowercase, for AM or PM)</td></tr>
<tr><th>( ... )</th><td>only renders the enclosed string if one or more non-zero digits</td></tr>
</table>

These formatting characters are only available to moments generated via the API as well as moments created with one of the [special moment constructors](moment#creating).


## Formatting ranges

Many parts of the API accept formatting strings for *ranges*, two dates that denote a start and end time. Some examples include [titleFormat](titleFormat) and [timeFormat](timeFormat).

In this scenario, FullCalendar intelligently inserts a dash between the two dates, yielding something like `"Sep 2 - 9 2013"`. Internally, [formatRange](formatRange) is used for this.
