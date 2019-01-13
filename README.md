# calendar-preview-widget
A widget for HABPanel which shows a preview of up to 10 upcoming calendar events. 

## Features
- Show a preview of up to 10 upcoming events with name and start date
- Display of event start and end time can be disabled 
- Title customizable, optionally with hyperlink to source calendar
- Custom date and time pattern
- Multiple widgets on the same dashboard with different styles      



![Sample screenshot](https://github.com/jep42/calendar-preview-widget/blob/master/widget-sample-screenshot.png "Sample screenshot")

## Installation
Via HABPanel widget gallery
- Add widget > user-defined widgets > More...
- Paste GitHub repository URL and press 'Go'
- 'Import widget'

## Widget settings

### General settings
Some general settings like the number of events that should be displayed (up to 10).

### Header settings
The header text as well as its color and size and optionally the URL to the calendar. If URL is given the header line of the widget will be rendered as hyperlink.

### Date settings
Date pattern as well as color and size of the date string.

### Time settings
Whether the event time should be shown and time pattern as well as its color and size.

### Name settings
Color and size of the event name.

### Events
OpenHab items which hold information about the event. For each event the widget can show name, start and end date and it is expected that these three types of information are represented by dedicated items which follow a special naming convention like so:
- *<item_name1>* => holds the name of the event (data type: String) 
- *<item_name1>***_start** => holds the start date of the event (data type: DateTime)  
- *<item_name1>***_end** => holds the end date of the event (data type: DateTime)

Example items configuration according to this convenion:  

```
String caldavEvent1         <calendar>	{ caldavPersonal="calendar:personal type:EVENT eventNr:1 value:NAME " }
DateTime caldavEvent1_start <calendar>	{ caldavPersonal="calendar:personal type:EVENT eventNr:1 value:START" }
DateTime caldavEvent1_end   <calendar>	{ caldavPersonal="calendar:personal type:EVENT eventNr:1 value:END" }
```















