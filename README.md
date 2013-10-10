摘要
====

来源： [DATE PICKER](http://www.eyecon.ro/datepicker/)

这是一个基于jQuery的日历插件。原始的版本只能支持jQuery1.7.2或之前的版本。

本改进后的版本支持jQuery1.4.3以后的版本。

本版本和官方版本有出入。

日期：2013-10-10


文档说明
========

应用
----

在页面中引入Javascript和CSS文件，并且按照站点的主题样式编辑CSS和修复CSS文件中图片的路径。

```HTML
<link rel="stylesheet" media="screen" type="text/css" href="css/datepicker.css" />
<script type="text/javascript" src="js/datepicker.js"></script>
```
                
调用代码
--------

你需要做的仅仅是利用jQuery指定一个需要调用日历插件的元素。

```JS
$('input').DatePicker(options);
```
                
选项
----

A hash of parameters. All parameters are optional.

* `eventName`   string  指定需要调用日历的期望事件。默认是'click'
* `date`    String, Date or array   The selected date(s) as string (will be converted to Date object based on teh format suplied) and Date object for single selection, as Array of strings or Date objects
* `flat`    boolean Whatever if the date picker is appended to the element or triggered by an event. Default false
* `start`   integer 指定一周的第一天。 默认是1（星期一）
* `prev`    string  HTML inserted to previous links. Default '◀' (UNICODE black left arrow)
* `next`    string  HTML inserted to next links. Default '▶' (UNICODE black right arrow)
* `mode`    string ['single'|'multiple'|'range']    Date selection mode. Default 'single'
* `view`    string ['days'|'months'|'years']    Start view mode. Default 'days'
* `calendars`   integer Number of calendars to render inside the date picker. Default 1
* `format`  string  Date format. Default 'Y-m-d'
* `position`    string ['top'|'left'|'right'|'bottom']  Date picker's position relative to the trigegr element (non flat mode only). Default 'bottom'
* `locale`  hash    Location: provide a hash with keys 'days', 'daysShort', 'daysMin', 'months', 'monthsShort', 'week'. Default english
* `onShow`  function    当日历显示时的回调函数。
* `onBeforeShow`    function    日历显示之前的回调函数。
* `onHide`  function    当日历隐藏时的回调函数
* `onChange`    function    当日期改变时的回调函数
* `onRender`    function    Callback function triggered when the date is rendered inside a calendar. It should return and hash with keys: 'selected' to select the date, 'disabled' to disable the date, 'className' for additional CSS class

Set date
--------

If you want to set a diferent date selection.

```JS
$('input').DatePickerSetDate(date, shiftTo);
```

The 'date' argument is the same format as the option 'date' and the 'shiftTo' argument (boolean) moves the curent month view to the date selection provided.

Get date
--------

Get date selection.

```JS
$('input').DatePickerGetDate(formated);
```

Set 'formated' to true if you whant to get teh selection formated.

Show and hide date picker
-------------------------

Show or hide a date picker.

```JS
$('input').DatePickerShow();
$('input').DatePickerHide();
```

Clear multiple selection
------------------------

Clear selection in multiple and range mode

```JS
$('#datepicker').DatePickerClear();
```


* * * * *

Abstract
========

Origin: [DATE PICKER](http://www.eyecon.ro/datepicker/)

This is a jQuery plugin of calendar. The origin version only support lte jQuery 1.7.2 version. 

This version can support gte jQuery 1.4.3 versions.

This version is not same as the raw version.

Date: Oct 10th, 2013.


Document
========

Implement
---------

Attach the Javascript and CSS files to your document. Edit CSS file and fix the paths to images and change colors to fit your site theme.

```HTML
<link rel="stylesheet" media="screen" type="text/css" href="css/datepicker.css" />
<script type="text/javascript" src="js/datepicker.js"></script>
```
                
Invocation code
---------------

All you have to do is to select the elements in a jQuery way and call the plugin.

```JS
$('input').DatePicker(options);
```
                
Options
-------

A hash of parameters. All parameters are optional.

* `eventName`   string  The desired event to trigger the date picker. Default: 'click'
* `date`    String, Date or array   The selected date(s) as string (will be converted to Date object based on teh format suplied) and Date object for single selection, as Array of strings or Date objects
* `flat`    boolean Whatever if the date picker is appended to the element or triggered by an event. Default false
* `start`   integer The day week start. Default 1 (monday)
* `prev`    string  HTML inserted to previous links. Default '◀' (UNICODE black left arrow)
* `next`    string  HTML inserted to next links. Default '▶' (UNICODE black right arrow)
* `mode`    string ['single'|'multiple'|'range']    Date selection mode. Default 'single'
* `view`    string ['days'|'months'|'years']    Start view mode. Default 'days'
* `calendars`   integer Number of calendars to render inside the date picker. Default 1
* `format`  string  Date format. Default 'Y-m-d'
* `position`    string ['top'|'left'|'right'|'bottom']  Date picker's position relative to the trigegr element (non flat mode only). Default 'bottom'
* `locale`  hash    Location: provide a hash with keys 'days', 'daysShort', 'daysMin', 'months', 'monthsShort', 'week'. Default english
* `onShow`  function    Callback function triggered when the date picker is shown
* `onBeforeShow`    function    Callback function triggered before the date picker is shown
* `onHide`  function    Callback function triggered when the date picker is hidden
* `onChange`    function    Callback function triggered when the date is changed
* `onRender`    function    Callback function triggered when the date is rendered inside a calendar. It should return and hash with keys: 'selected' to select the date, 'disabled' to disable the date, 'className' for additional CSS class

Set date
--------

If you want to set a diferent date selection.

```JS
$('input').DatePickerSetDate(date, shiftTo);
```

The 'date' argument is the same format as the option 'date' and the 'shiftTo' argument (boolean) moves the curent month view to the date selection provided.

Get date
--------

Get date selection.

```JS
$('input').DatePickerGetDate(formated);
```

Set 'formated' to true if you whant to get teh selection formated.

Show and hide date picker
-------------------------

Show or hide a date picker.

```JS
$('input').DatePickerShow();
$('input').DatePickerHide();
```

Clear multiple selection
------------------------

Clear selection in multiple and range mode

```JS
$('#datepicker').DatePickerClear();
```