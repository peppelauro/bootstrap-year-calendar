# bulma-year-calendar
A fully customizable year calendar widget, for bulma !
Based on bootstrap-year-calendar by Paul-DS.


![alt tag](http://www.bootstrap-year-calendar.com/img/calendar.png)

## Requirements

This plugin requires the following libraries :
- ~~Bootstrap v3.0.0~~ Bulma v0.6.2 or later
- jQuery v1.8.0 or later

## Installation
You can get the widget using the following methods:
- From the [GitHub repository](https://github.com/peppelauro/bulma-year-calendar/releases) ~~or the [official website](http://www.bootstrap-year-calendar.com/#Download).~~
- From the Node package manager, using the following command: `npm install bulma-year-calendar`
- From Bower, using the following command: `bower install bulma-year-calendar`

## Usage

You can create a calendar using the following javascript code :
```
$('.calendar').calendar()
```
or
```
$('.calendar').calendar(options)
```
or with the `data-provide` html attribute 
```
<div data-provide="calendar"></div>
```

## Options
All options can be set at initialization :
```
    $('#element').calendar({ /* Set options here */ })
```    
Or using the get/set methods present for each option.

### allowOverlap
Type: Boolean  
Default: true  
Get/Set methods: getAllowOverlap(), setAllowOverlap()  

Specifies whether the user can select a range which overlapping an other element present in the datasource.

### alwaysHalfDay
Type: Boolean  
Default: false  
Get/Set methods: getAlwaysHalfDay(), setAlwaysHalfDay()  

Specifies whether the beginning and the end of each datasource should be displayed as half selected day.

### contextMenuItems
Type: Array of: { text: String, click: function(dataSourceElement), subMenu: [] }  
Default: false  
Get/Set methods: getContextMenuItems(), setContextMenuItems()  

Specifies the items of the default context menu.  
The click event is called with the selected data source element. Each menu item can contain sub-items, which can themselves contain sub-items, etc...  
Don't forget to enable the enableContextMenu option to be able to use the context menu.

### customDayRenderer
Type: function(element, date)  
Default: null  
Get/Set methods: getCustomDayRenderer(), setCustomDayRenderer()  

Specify a custom renderer for days.  
This function is called during render for each day.

### customDataSourceRenderer
Type: function(element, date, events)  
Default: null  
Get/Set methods: getCustomDataSourceRenderer(), setCustomDataSourceRenderer()  

Specify a custom renderer for data source.  
Works only with the style set to "custom".  
This function is called during render for each day containing at least one event.

### dataSource
Type: Array of: { startDate: Date, endDate: Date, name: String, ... }  
Default: []  
Get/Set methods: getDataSource(), setDataSource()  

The elements that must be displayed on the calendar. The objects present in the array must contain a start date and an end date (and a title if you want to use the default context menu), but they can contain other properties.

### disabledDays
Type: Array of Date  
Default: []  
Get/Set methods: getDisabledDays(), setDisabledDays()  

The days that must be displayed as disabled.

### displayWeekNumber
Type: Boolean  
Default: false  
Get/Set methods: getDisplayWeekNumber(), setDisplayWeekNumber()  

Specifies whether the weeks number are displayed.

### enableContextMenu
Type: Boolean  
Default: false  
Get/Set methods: getEnableContextMenu(), setEnableContextMenu()  

Specifies whether the default context menu must be displayed when right clicking on a day.

### enableRangeSelection
Type: Boolean  
Default: false  
Get/Set methods: getEnableRangeSelection(), setEnableRangeSelection()  

Specifies whether the user can make range selection.

### language
Type: String  
Default: en  
Get/Set methods: getLanguage(), setLanguage()  

The language/culture used for calendar rendering. The implemented language are the following :

English  
French  
To use a language, you need to include the corresponding js file (bootstrap-year-calendar.XX.js or bootstrap-year-calendar.XX.min.js).  
If the used language contains some special characters, don't forget to use the charset="UTF-8" attribute on the script tag.  
If a non implemented language is specified, the default language will be used (english).  

### maxDate
Type: Date  
Default: null  
Get/Set methods: getMaxDate(), setMaxDate()  

The date until which days are enabled (user can select dates, etc...). User cannot not access the years after the maximum date.

### minDate
Type: Date  
Default: null  
Get/Set methods: getMinDate(), setMinDate()  

The date from which days are enabled (user can select dates, etc...). User cannot not access the years before the minimum date.

### roundRangeLimits
Type: Boolean  
Default: false  
Get/Set methods: getRoundRangeLimits(), setRoundRangeLimits()  

Specifies whether the beginning and the end of each range should be displayed as rounded cells.

### startYear
Type: Number  
Default: Current year  
Get/Set methods: getYear(), setYear()  

The year on which the calendar should be opened.

### style
Type: String  
Default: 'border'  
Get/Set methods: getStyle(), setStyle()  

Specifies the style used for displaying datasource:  

border: a colored border is displayed under the number of the day. This option allows to display several elements on a same day.  
background: a colored background is displayed behind the day. This option allows to display only one element on a same day.  
