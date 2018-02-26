---
title: Moment Object
type: guide
---

A Moment object represents a point in time, like the native [Date Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date), but is far superior.

This functionality is provided by [MomentJS](http://momentjs.com/), a third-party open-source library. FullCalendar extends this functionality a bit to accomodate for ambiguously-timed and ambiguously-zoned moments.

[**See the MomentJS docs &raquo;**](http://momentjs.com/docs/)

In the API, most options that accept a Moment will also conveniently accept anything that the `moment()` constructor accepts, including:

- date strings (ISO8601 is **highly** recommended)
- unix offsets (milliseconds since the Unix Epoch)
- native Date objects


<h2 id='creating'>Creating Moments from scratch</h2>

Most of the time you won't have to worry about instantiating your own Moments. For example, when specify [event array](events-array) data, you can just write ISO8601 strings and let FullCalendar handle the parsing.

However, creating Moments from scratch is sometimes necessary. Since Moment is a dependency of FullCalendar, the global `moment` constructor will likely be available to you. You should be able to create new Moments from scratch like this:

```js
var m = moment();
```

To create a moment with FullCalendar's [extended formatting](date-formatting-string) and "ambiguous" functionality (see below), use FullCalendar's version of the `moment`, `moment.utc`, and `moment.parseZone` constructors:

```js
var noTime = $.fullCalendar.moment('2014-05-01');
var local = $.fullCalendar.moment('2014-05-01T12:00:00');
var utc = $.fullCalendar.moment.utc('2014-05-01T12:00:00');
var noTZ = $.fullCalendar.moment.parseZone('2014-05-01T12:00:00');
```

To create a moment with extended functionality that is already scoped within a given calendar's [timezone](timezone) and [locale](locale) settings, use the `Calendar` object's version of the `moment` constructor:

```js
var calendar = $('#calendar').fullCalendar('getCalendar');
var m = calendar.moment();
```

<h2 id='ambiguously-timed'>Ambiguously-timed Moments</h2>

For FullCalendar, the Moment object has been extended to represent a moment without a time, or an "ambigously-timed moment". Under the hood, these moments are represented in [UTC-mode](http://momentjs.com/docs/#/parsing/utc/) with a time of `00:00:00`.

To create one, you can use FullCalendar's version of the `moment`, `moment.utc`, or `moment.parseZone` constructor in tandem with an ISO8601 string without a time part:

```js
var m = $.fullCalendar.moment('2014-01-22');
m.hasTime();
=> false
```

As you can see, you can query if a moment is ambiguously-timed by using the `hasTime` method. This method is only available on moments created through one of FullCalendar's moment constructors.

You can also convert a timed moment to ambiguous by using the `stripTime` method. This method is only available on moments created through one of FullCalendar's moment constructors.

```js
var m = $.fullCalendar.moment('2014-01-22T05:00:00');
m.stripTime();
m.hasTime();
=> false
```

The `format` and `toISOString` methods have been modified so that ambiguously-timed moments do to not return a time part in the string:

```js
m.format();
=> "2013-01-22"
```

<h2 id='ambiguously-zoned'>Ambiguously-zoned Moments</h2>

The moment object has also been extended to represent a date with no specified timezone. Under the hood, these moments are represented in [UTC-mode](http://momentjs.com/docs/#/parsing/utc/).

To create one, you can use FullCalendar's version of the `moment.parseZone` constructor in tandem with an ISO8601 string without a timezone offset part:

```js
var m = $.fullCalendar.moment.parseZone('2014-01-22T06:00:00');
m.hasZone();
=> false
```

As you can see, you can query if a moment is ambiguously-zoned by using the `hasZone` method. This method is only available on moments created through one of FullCalendar's moment constructors.

You can also convert unambiguous to ambiguous by using the `stripZone` method. This method is only available on moments created through one of FullCalendar's moment constructors.

```js
var m = $.fullCalendar.moment('2014-01-22T05:00:00-07:00');
m.stripZone();
m.hasZone();
=> false
```

The `format` and `toISOString` methods have been modified so that ambiguously-zoned moments do not return a timezone offset part in the string:

```js
m.format();
=> "2014-01-22T05:00:00"
```

## Other extensions

Extended moments will have the `time` utility available to them, which is a getter/setter for the hours/minutes/seconds/milliseconds part of the moment. It accepts/returns a [Duration](moment-duration)-ish object representing the time:

```js
var m = moment();
m.time('05:30:00');
m.time(); // returns Duration with 05:30:00
```
