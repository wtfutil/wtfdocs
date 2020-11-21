![gcal](/assets/services/gcal.png){: align=left width=128 height=128}

# Google Calendar

Displays your upcoming Google calendar events.

**Note:** Setting up access to Google Calendars for Go is a bit unobvious. Check out Google's [Go Quickstart](https://developers.google.com/calendar/quickstart/go), and follow `Enable The Google Calendar API`. 

The configuration file downloaded is the file you use for the `secretFile` configuration option.

## Configuration

```yaml
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
```

## Screenshots

<img class="screenshot" src="/assets/modules/gcal.png" width="320" height="389" alt="gcal screenshot" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
      {% with name="colors.eventTime", desc="<em>Optional</em> The default color for calendar event time." %}
        {% include "attributes/colors/custom.md" %}
      {% endwith %}

      {% with name="colors.description", desc="<em>Optional</em> The default color for calendar event description." %}
        {% include "attributes/colors/custom.md" %}
      {% endwith %}

      {% with name="colors.past", desc="<em>Optional</em> The color for calendar events that have passed." %}
        {% include "attributes/colors/custom.md" %}
      {% endwith %}

      {% with name="colors.title", desc="<em>Optional</em> The default colour for calendar event titles." %}
        {% include "attributes/colors/custom.md" %}
      {% endwith %}

      {% with name="colors.highlights", desc="<em>Optional</em> A list of arrays that define a regular expression pattern and a color. If a calendar event title matches a regular expression, the title will be drawn in that colour. Over-rides the default title colour.", value="A valid regular expression, or any <a href='https://en.wikipedia.org/wiki/X11_color_names'>X11 color</a> name." %}
        {% include "attributes/custom.md" %}
      {% endwith %}

      {% with name="calendarReadLevel", desc="<em>Optional</em> The calender read level specifies level you want to read events. Default: <code>reader</code>.", value="<code>reader</code>, <code>writer</code>" %}
        {% include "attributes/custom.md" %}
      {% endwith %}

      {% with name="conflictIcon", desc="<em>Optional</em> The icon displayed beside calendar events that have conflicting times (they intersect or overlap in some way).", value="Any displayable unicode character." %}
        {% include "attributes/custom.md" %}
      {% endwith %}

      {% with name="currentIcon", desc="<em>Optional</em> The icon displayed beside the current calendar event.", value="Any displayable unicode character." %}
        {% include "attributes/custom.md" %}
      {% endwith %}

      {% with name="displayResponseStatus", desc="<em>Optional</em> Whether or not to display your response status to the calendar event. Default: <code>true</code>.", value="<code>true</code>, <code>false</code>" %}
        {% include "attributes/custom.md" %}
      {% endwith %}

      {% with name="email", desc="The email address associated with your Google account. Necessary for determining <code>responseStatus</code>.", value="A valid email address string." %}
        {% include "attributes/custom.md" %}
      {% endwith %}

      {% with name="eventCount", desc="<em>Optional</em> The number of calendar events to display.", value="Any positive integer." %}
        {% include "attributes/custom.md" %}
      {% endwith %}

      {% include "attributes/hourFormat.md" %}

      {% with name="multiCalendar", desc="<em>Optional</em> Whether or not to display your primary calendar or all calendars you have access to. Default: <code>false</code>.", value="<code>true</code>, <code>false</code>" %}
        {% include "attributes/custom.md" %}
      {% endwith %}

      {% with name="secretFile", desc="Your <a href='https://developers.google.com/calendar/quickstart/go'>Google client secret</a> JSON file.", value="A string representing a file path to the JSON secret file." %}
        {% include "attributes/custom.md" %}
      {% endwith %}

      {% with name="showDeclined", desc="<em>Optional</em> Whether or not to display events you’ve declined to attend. Default: <code>true</code>.", value="<code>true</code>, <code>false</code>" %}
        {% include "attributes/custom.md" %}
      {% endwith %}

      {% with name="showEndTime", desc="<em>Optional</em> Whether or not to display the event end time. Default: <code>false</code>.", value="<code>true</code>, <code>false</code>" %}
        {% include "attributes/custom.md" %}
      {% endwith %}

      {% include "attributes/timezone.md" %}

      {% with name="withLocation", desc="<em>Optional</em> Whether or not to show the location of the appointment. Default: <code>true</code>.", value="<code>true</code>, <code>false</code>" %}
        {% include "attributes/custom.md" %}
      {% endwith %}
    </tbody>
</table>

{% set src="gcal" %}
{% include "src_path.md" %}
