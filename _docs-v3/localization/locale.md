---
title: locale
version_notes: changed in 3.0 from lang
---

Customize the language and localization options for the calendar.

<div class='spec' markdown='1'>
A String locale code. *default*: `"en"`
</div>

This option affects many things such as:

- the text in buttons, as defined by [header](header)
- text that contains month or day-of-week strings
- date formatting strings, such as [timeFormat](timeFormat)
- [weekNumberCalculation](weekNumberCalculation)
- [firstDay](firstDay)


## How to use other locales

You will need to load the locale JavaScript data file in order to use it.
These files are included with the FullCalendar download in the `locale/` directory.
They must be loaded via a `<script>` tag after the main FullCalendar library is loaded.

    <script src='fullcalendar/fullcalendar.js'></script>

```html
<script src='fullcalendar/locale/es.js'></script>
<script>

  $(function() {

    $('#calendar').fullCalendar({
    });

  });

</script>
```

If you are simply loading one locale, you do *not* need to specify the `locale` option. FullCalendar will look at the most recent locale file loaded and use it.

However, if more than one locale file is loaded, or the combined `locale-all.js` file is loaded, you must explicitly specify which locale to use via the `locale` option:

```html
<script src='fullcalendar/fullcalendar.js'></script>
<script src='fullcalendar/locale-all.js'></script>
<script>

  $(function() {

    $('#calendar').fullCalendar({
      locale: 'es'
    });

  });

</script>
```

For more information, [view a live demo](locale-demo).


## MomentJS and jQuery UI Datepicker

When you load a FullCalendar locale file, it also loads the translations
for MomentJS and jQuery UI Datepicker (if the library is already on the page).
Just make sure to include the `<script>` tags for Moment and Datepicker before
you include FullCalendar's locale file:

    <script src='lib/moment.js'></script>

```html
<script src='lib/jquery-ui.custom-datepicker.js'></script>
<script src='fullcalendar/fullcalendar.js'></script>
<script src='fullcalendar/locale-all.js'></script>
```
