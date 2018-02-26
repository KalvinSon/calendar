---
permalink: /support
is_support: true
title: Support
layout: text
---

{% assign needs_core_version = site.data.releases.fullcalendar-scheduler[0].needsCore %}

<div class='sidenote-layout'>
<div class='sidenote-layout__main' markdown='1'>

## Getting Help

Have a tough problem you can't figure out? Try searching the [documentation]({{ site.baseurl }}/docs) first. If you can't find what you're looking for, try Googling around.

If you still can't find an answer, post your question on the [StackOverflow **fullcalendar** tag](http://stackoverflow.com/questions/tagged/fullcalendar'). When entering a new question, make sure you tag it with **fullcalendar**.

You can improve your chances of getting an answer by 900% if you [post a reduced test case &raquo;]({{ site.baseurl }}/reduced-test-cases)

## Reporting a Bug

Think you've found a bug? Please carefully follow the [bug report instructions &raquo;]({{ site.baseurl }}/reporting-bugs)

## Requesting a Feature

Have an idea for a new feature? Please carefully follow the [feature request instructions &raquo;]({{ site.baseurl }}/requesting-features)

## Browser Testing & Version Compatibility

The latest version of FullCalendar is compatible with:

- Firefox, Chrome, Safari, IE 9+
- jQuery 2.0.0+
- Moment 2.9.0+

The latest version of [FullCalendar Scheduler]({{ site.baseurl }}/scheduler) requires:

- FullCalendar Core version >={{ needs_core_version }}

</div>
<div class='sidenote-layout__sidenote' markdown='1'>

### Need help with the Scheduler?

<a href='{{ site.baseurl }}/scheduler/purchase'>
  The Scheduler plugin comes with<br />1 year of email support
</a>

</div>
</div>
