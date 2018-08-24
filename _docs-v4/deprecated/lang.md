---
title: lang
---

Customize the language and localization options for the calendar.

<div class='removed-notice'>
This settings has been renamed to <a href='locale'>locale</a> in v3.
Also, the <code>lang.js</code> and <code>/lang/*.js</code> files have been similarly renamed.
</div>

<div class='spec' markdown='1'>
A String language code. *default*: `"en"`
</div>

This option affects many things such as:

- the text in buttons, as defined by [header](header)
- text that contains month or day-of-week strings
- date formatting strings, such as [timeFormat](timeFormat)
- [weekNumberCalculation](weekNumberCalculation)
- [firstDay](firstDay)


## How to use other languages

You will need to load the language's JavaScript data file in order to use it.
These files are included with the FullCalendar download in the `lang/` directory.
They must be loaded via a `<script>` tag after the main FullCalendar library is loaded.

    <script src='fullcalendar/fullcalendar.js'></script>

```html
<script src='fullcalendar/lang/es.js'></script>
<script>

  $(function() {

    $('#calendar').fullCalendar({
    });

  });

</script>
```

If you are simply loading one language, you do *not* need to specify the `lang` option. FullCalendar will look at the most recent language file loaded and use it.

However, if more than one language file is loaded, or the combined `all.js` file is loaded, you must explicitly specify which language to use via the `lang` option:

```html
<script src='fullcalendar/fullcalendar.js'></script>
<script src='fullcalendar/lang-all.js'></script>
<script>

  $(function() {

    $('#calendar').fullCalendar({
      lang: 'es'
    });

  });

</script>
```


## MomentJS and jQuery UI Datepicker

When you load a FullCalendar language file, it also loads the translations
for MomentJS and jQuery UI Datepicker (if the library is already on the page).
Just make sure to include the `<script>` tags for Moment and Datepicker before
you include FullCalendar's language file:

    <script src='lib/moment.js'></script>

```html
<script src='lib/jquery-ui.custom-datepicker.js'></script>
<script src='fullcalendar/fullcalendar.js'></script>
<script src='fullcalendar/lang-all.js'></script>
```
