---
title: buttons
---

Defines the buttons and button-text at the top of the calendar.

<div class='removed-notice'>
This option was removed in 1.3 in favor of <a href='header'>header</a> and <a href='buttonText'>buttonText</a>.
</div>

<div class='spec' markdown='1'>
Boolean/Object, *default*: `true`
</div>

`true` will display a previous-month, next-month, and "today" button. The "today" button will only be visible for months other than the current.

`false` will display absolutely no buttons.

An object hash can be provided to display only *certain* buttons. The hash can have the following properties:

```js
{
  today:     bool/string,
  prevYear:  bool/string,
  prevMonth: bool/string,
  nextMonth: bool/string,
  nextYear:  bool/string
}
```

A value of `false` will not display the button. A value of `true` will display the button with some default text. A string value will display the button *and* customize its text.
