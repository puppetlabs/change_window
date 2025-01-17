# Reference

<!-- DO NOT EDIT: This document was generated by Puppet Strings -->

## Table of Contents

### Defined types

* [`change_window::apply`](#change_windowapply)

### Functions

* [`change_window::change_window`](#change_windowchange_window): Provides change_window function that allows you to check current time against change window
* [`change_window::merge_change_windows`](#change_windowmerge_change_windows): Creates complex change windows by merging a series of windows together

## Defined types

### <a name="change_windowapply"></a>`change_window::apply`

The change_window::apply class.

#### Parameters

The following parameters are available in the `change_window::apply` defined type:

* [`change_window_set`](#change_window_set)
* [`class_list`](#class_list)

##### <a name="change_window_set"></a>`change_window_set`

Data type: `Any`

An array of change_window names to be merged.

##### <a name="class_list"></a>`class_list`

Data type: `Any`

An array of classes to be applied when within the change_window.

## Functions

### <a name="change_windowchange_window"></a>`change_window::change_window`

Type: Ruby 4.x API

Provides change_window function that allows you to check current time against change window

#### `change_window::change_window(String $timezone, String $window_type, Hash $window_wday, Hash $window_time, Optional[Array] $window_week_val, Optional[Array] $window_month_val, Optional[Array] $time)`

The change_window::change_window function.

Returns: `String` Returns true or false as string if the time is within the change window

##### `timezone`

Data type: `String`

the timezone offset to use when timestamp is generated for comparing to change window

##### `window_type`

Data type: `String`

type of window, either 'per_day' or 'window'

##### `window_wday`

Data type: `Hash`

containing start and end days of week for the change window

##### `window_time`

Data type: `Hash`

containing start and end times of day for the change window

##### `window_week`

Data type: `Array`

[Optional] list of weeks in month for the change window

##### `window_month`

Data type: `Array`

[Optional] list of months in year for the change window

##### `time`

Data type: `Optional[Array]`

[Optional] array representing a fixed time to test against

##### `window_week_val`

Data type: `Optional[Array]`



##### `window_month_val`

Data type: `Optional[Array]`



### <a name="change_windowmerge_change_windows"></a>`change_window::merge_change_windows`

Type: Ruby 4.x API

Creates complex change windows by merging a series of windows together

#### `change_window::merge_change_windows(Array *$change_windows)`

The change_window::merge_change_windows function.

Returns: `String` Returns true or false as string if the time is within the merged change window

##### `*change_windows`

Data type: `Array`

a list of change windows to merge

