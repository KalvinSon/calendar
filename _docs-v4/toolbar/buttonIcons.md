---
title: buttonIcons
---

Icons that will be displayed in buttons of the header/footer.

<div class='spec' markdown='1'>
Object, *default:*

```js
{
  prev: 'left-single-arrow',
  next: 'right-single-arrow',
  prevYear: 'left-double-arrow',
  nextYear: 'right-double-arrow'
}
```
</div>

This setting only takes affect when [theme](theme) is `false`. If you want to change icons when [theme](theme) is `true`, use [themeButtonIcons](themeButtonIcons) instead.

A hash must be supplied that maps button names (from the [header](header)) to icon strings. These icon string are transformed into classNames which are styled by FullCalendar's CSS.

If a button does not have an entry, it falls back to using [buttonText](buttonText).

If you would prefer not to display any icons and would rather use `buttonText` instead, you can set the `buttonIcons` option to `false`.
