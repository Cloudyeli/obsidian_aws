## AWS Change Clendar
#(AWS [[Systems Manager]])

Change Calendar, a capability of AWS Systems Manager, allows you to set up date and time ranges when actions you specify (for example, in Systems Manager [[Automation]] runbooks) might or might not be performed in your AWS account. In Change Calendar, these ranges are called _events_. When you create a Change Calendar entry, you're creating a [[Systems Manager]] document of the type `ChangeCalendar`. In Change Calendar, the document stores iCalendar 2.0 data in plaintext format. Events that you add to the Change Calendar entry become part of the document. To get started with Change Calendar, open the Systems Manager console. In the navigation pane, choose **Change Calendar**.

You can create a calendar and its events in the Systems Manager console. You can also import an iCalendar (`.ics`) file that you have exported from a supported third-party calendar provider to add its events to your calendar. Supported providers include Google Calendar, Microsoft Outlook, and iCloud Calendar.

A Change Calendar entry can be one of two types:

**`DEFAULT_OPEN`**, or Open by default

All actions can run by default, except during calendar events. During events, the state of a `DEFAULT_OPEN` calendar is `CLOSED` and events are blocked from running.

**`DEFAULT_CLOSED`**, or Closed by default

All actions are blocked by default, except during calendar events. During events, the state of a `DEFAULT_CLOSED` calendar is `OPEN` and actions are permitted to run.