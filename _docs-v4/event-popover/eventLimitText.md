---
title: eventLimitText
since_version: 2.1.0
---

Determines the text of the link created by the [eventLimit](eventLimit) setting.

<div class='spec' markdown='1'>
String, Function. *default:* `"more"`
</div>

If a string is specified, the resulting text will be prepended with the number of events being obscured, like "+2", resulting in something like "+2 more".

If a function is specified, the function will be given a single argument, the number of events being obscured, and must return the final text string to be used.

The default value of this option is affected by the current [locale](locale).
