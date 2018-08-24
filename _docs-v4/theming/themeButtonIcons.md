---
title: themeButtonIcons
---

Determines which icons are displayed in buttons of the header/footer when jQuery UI theming is on.

<div class='spec' markdown='1'>
Object, *default:*

```js
{
  prev: 'circle-triangle-w',
  next: 'circle-triangle-e',
  prevYear: 'seek-prev',
  nextYear: 'seek-next'
}
```
</div>

This option only applies to calendars that have [themeSystem](themeSystem) set to `'jquery-ui'`.

A hash must be supplied that maps button names (from the [header](header)) to icon strings. The icon strings determine the CSS class that will be used on the button. For example, the string `'circle-triangle-w'` will result in the class `'ui-icon-circle-triangle-w'`.

If a button does not have an entry, it falls back to using [buttonText](buttonText).

If you are using a jQuery UI theme and would prefer not to display any icons and would rather use `buttonText` instead, you can set the `themeButtonIcons` option to `false`.
