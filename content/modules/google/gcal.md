---
title: "Google Calendar"
date: 2018-05-10T08:25:33-07:00
draft: false
weight: 10
---

Displays your upcoming Google calendar events.

**Note:** Setting up access to Google Calendars for Go is a bit unobvious. Check out Google's [Go Quickstart](https://developers.google.com/calendar/quickstart/go), and follow `Enable The Google Calendar API`. 

The configuration file downloaded is the file you use for the `secretFile` configuration option.

## Configuration

{{< code lang="yaml" >}}
gcal:
  colors:
    title: "red"
    eventTime: "lightblue"
    description: "yellow"
    highlights:
    - ['1on1|1\/11', 'green']
    - ['apple|google|aws', 'blue']
    - ['interview|meet', 'magenta']
    - ['lunch', 'yellow']
    past: "gray"
  calendarReadLevel: "reader"
  conflictIcon: "🚨"
  currentIcon: "💥"
  displayResponseStatus: true
  email: "chriscummer@me.com"
  enabled: true
  eventCount: 15
  hourFormat: "12"
  multiCalendar: true
  position:
    top: 0
    left: 0
    height: 4
    width: 1
  refreshInterval: 300
  secretFile: "~/.config/wtf/gcal/client_secret.json"
  showDeclined: true
  showEndTime: false
  timezone: "America/Vancouver"
  withLocation: true
{{< /code >}}

## Screenshots

<img class="screenshot" src="/imgs/modules/gcal.png" width="320" height="389" alt="gcal screenshot" />

{{% attributes %}}
  {{< attributes/border >}}
  {{< attributes/colors/custom name="colors.eventTime" desc="The default color for calendar event time." >}}
  {{< attributes/colors/custom name="colors.description" desc="The default color for calendar event description." >}}
  {{< attributes/colors/custom name="colors.past" desc="The color for calendar events that have passed." >}}
  {{< attributes/colors/custom name="colors.title" desc="The default colour for calendar event titles." >}}

  <tr>
    <td>`colors.highlights`</td>
    <td>A list of arrays that define a regular expression pattern and a color. If a calendar event title matches a regular expression, the title will be drawn in that colour. Over-rides the default title colour.</td>
    <td>[a valid regular expression, any <a href="https://en.wikipedia.org/wiki/X11_color_names">X11 color</a> name.]</td>
  </tr>

  {{< attributes/custom name="calendarReadLevel" desc="_Optional_ The calender read level specifies level you want to read events. Default: reader." value="reader, writer" >}}
  {{< attributes/custom name="conflictIcon" desc="_Optional_ The icon displayed beside calendar events that have conflicting times (they intersect or overlap in some way)." value="Any displayable unicode character." >}}
  {{< attributes/custom name="currentIcon" desc="_Optional_ The icon displayed beside the current calendar event." value="Any displayable unicode character." >}}
  {{< attributes/custom name="displayResponseStatus" desc="_Optional_ Whether or not to display your response status to the calendar event. Default: true." value="true, false" >}}
  {{< attributes/custom name="email" desc="The email address associated with your Google account. Necessary for determining `responseStatus`." value="A valid email address string.">}}
  {{< attributes/enabled >}}
  {{< attributes/custom name="eventCount" desc="The number of calendar events to display." value="Any positive integer">}}
  {{< attributes/focusChar >}}
  {{< attributes/hourFormat >}}
  {{< attributes/custom name="multiCalendar" desc="_Optional_ Whether or not to display your primary calendar or all calendars you have access to. Default: false." value="true, false">}}
  {{< attributes/position >}}
  {{< attributes/refreshInterval >}}

  <tr>
    <td>`secretFile`</td>
    <td>Your <a href="https://developers.google.com/calendar/quickstart/go">Google client secret</a> JSON file.</td>
    <td>A string representing a file path to the JSON secret file.</td>
  </tr>


  {{< attributes/custom name="showDeclined" desc="_Optional_ Whether or not to show the location of the appointment. Default: true." value="true, false" >}}
  {{< attributes/custom name="showEndTime" desc="_Optional_ Whether or not to display the event end time. Default: false." value="true, false" >}}

  {{< attributes/timezone >}}
  {{< attributes/custom name="withLocation" desc="_Optional_ Whether or not to show the location of the appointment. Default: true." value="true, false" >}}
{{% /attributes %}}

{{% sourcePath module="gcal" %}}