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

参数的哈希表。所有的参数均是可选的。

* `eventName`   string  指定需要调用日历的期望事件。默认是'click'
* `date`    String, Date or array   The selected date(s) as string (will be converted to Date object based on the format suplied) and Date object for single selection, as Array of strings or Date objects
* `flat`    boolean 是否将日历选择器设置成一个元素，亦或作为一个元素的事件。 默认是 false
* `start`   integer 指定一周的第一天。 默认是1（星期一）
* `prev`    string  前一项连接的HTML字符。 默认是 '◀' (UNICODE 黑色左箭头)
* `next`    string  后一项连接的HTML字符。 默认是 '▶' (UNICODE 黑色右箭头)
* `mode`    string ['single'|'multiple'|'range']    日期选择模式. 默认是 'single'
* `view`    string ['days'|'months'|'years']    开始的视图模式. 默认是 'days'
* `calendars`   integer 在日历选择区域中渲染的日历数量。 默认是 1
* `format`  string  日期格式. 默认是 'Y-m-d'
* `position`    string ['top'|'left'|'right'|'bottom']  日历相对触发元素的位置。(flat模式不支持本选项). 默认是 'bottom'
* `locale`  hash    Location: provide a hash with keys 'days', 'daysShort', 'daysMin', 'months', 'monthsShort', 'week'. 默认是 english
* `onShow`  function    当日历显示时的回调函数。
* `onBeforeShow`    function    日历显示之前的回调函数。
* `onHide`  function    当日历隐藏时的回调函数
* `onChange`    function    当日期改变时的回调函数
* `onRender`    function    Callback function triggered when the date is rendered inside a calendar. It should return and hash with keys: 'selected' to select the date, 'disabled' to disable the date, 'className' for additional CSS class

设置日期
--------

如果你想要设置一个不同的日期：

```JS
$('input').DatePickerSetDate(date, shiftTo);
```

`date`参数与选项`date`中的格式一致；`shiftTo`（布尔值）参数则表示是否从当前月移动到选择日期的月份视图。

获取日期
--------

获得选中的日期。

```JS
$('input').DatePickerGetDate(formated);
```

如果你想得到一个格式化好的日期，则需要讲formated设置为真。

显示或隐藏日历
--------------

显示或隐藏日历

```JS
$('input').DatePickerShow();
$('input').DatePickerHide();
```

清除多选
--------

在范围选择模式下清除多选。

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
* `date`    String, Date or array   The selected date(s) as string (will be converted to Date object based on the format suplied) and Date object for single selection, as Array of strings or Date objects
* `flat`    boolean Whatever if the date picker is appended to the element or triggered by an event. Default false
* `start`   integer The day week start. Default 1 (monday)
* `prev`    string  HTML inserted to previous links. Default '◀' (UNICODE black left arrow)
* `next`    string  HTML inserted to next links. Default '▶' (UNICODE black right arrow)
* `mode`    string ['single'|'multiple'|'range']    Date selection mode. Default 'single'
* `view`    string ['days'|'months'|'years']    Start view mode. Default 'days'
* `calendars`   integer Number of calendars to render inside the date picker. Default 1
* `format`  string  Date format. Default 'Y-m-d'
* `position`    string ['top'|'left'|'right'|'bottom']  Date picker's position relative to the trigger element (non flat mode only). Default 'bottom'
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

The 'date' argument is the same format as the option 'date' and the 'shiftTo' argument (boolean) moves the current month view to the date selection provided.

Get date
--------

Get date selection.

```JS
$('input').DatePickerGetDate(formated);
```

Set 'formated' to true if you want to get the selection formated.

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