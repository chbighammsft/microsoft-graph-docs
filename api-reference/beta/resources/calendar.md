# calendar resource type

A calendar which is a container for events.

### Methods

| Method       | Return Type  |Description|
|:---------------|:--------|:----------|
|[List calendars](../api/user_list_calendars.md)|[calendar](calendar.md) collection|Get all the user's calendars, or the calendars in the default or other specific calendar group.|
|[Create calendar](../api/user_post_calendars.md) |[calendar](calendar.md)| Create a new calendar in the default calendar group or specified calendar group.|
|[Get calendar](../api/calendar_get.md) | [calendar](calendar.md) |Read properties and relationships of calendar object.|
|[Update](../api/calendar_update.md) | [calendar](calendar.md)  |Update calendar object. |
|[Delete](../api/calendar_delete.md) | None |Delete calendar object. |
|[List calendarView](../api/calendar_list_calendarview.md) |[event](event.md) collection| Get the occurrences, exceptions, and single instances of events in a calendar view defined by a time range, from the user's primary calendar `(../me/calendarview)` or from a specified calendar.|
|[List events](../api/calendar_list_events.md) |[event](event.md) collection| Retrieve a list of events in a calendar.  The list contains single instance meetings and series masters.|
|[Create Event](../api/calendar_post_events.md) |[event](event.md)| Create a new Event in the default or specified calendar.|
|[Create single-value extended property](../api/singlevaluelegacyextendedproperty_post_singlevalueextendedproperties.md) |[calendar](calendar.md)  |Create one or more single-value extended properties in a new or existing calendar.   |
|[Get calendar with single-value extended property](../api/singlevaluelegacyextendedproperty_get.md)  | [calendar](calendar.md) | Get calendars that contain a single-value extended property by using `$expand` or `$filter`. |
|[Create multi-value extended property](../api/multivaluelegacyextendedproperty_post_multivalueextendedproperties.md) | [calendar](calendar.md) | Create one or more multi-value extended properties in a new or existing calendar.  |
|[Get calendar with multi-value extended property](../api/multivaluelegacyextendedproperty_get.md)  | [calendar](calendar.md) | Get a calendar that contains a multi-value extended property by using `$expand`. |

### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|canEdit|Boolean|True if the user can edit the calendar, false otherwise.|
|canShare|Boolean|True if the user can share the calendar, false otherwise.|
|canViewPrivateItems|Boolean|True if the user can view private items in the calendar, false otherwise.|
|changeKey|String|Identifies the version of the calendar object. Every time the calendar is changed, ChangeKey  changes as well. This allows Exchange to apply changes to the correct version of the object. Read-only.|
|color|String|Specifies the color theme to distinguish the calendar from other calendars in a UI. The property values are: LightBlue=0, LightGreen=1, LightOrange=2, LightGray=3, LightYellow=4, LightTeal=5, LightPink=6, LightBrown=7, LightRed=8, MaxColor=9, Auto=-1|
|id|String|The group's unique identifier. Read-only.|
|isDefaultCalendar|Boolean|True if this calendar is the user's default calendar, false otherwise.|
|isShared|Boolean|True if the calendar is shared with someone else, false otherwise.|
|isSharedWithMe|Boolean|True if the calendar is shared with the user, false otherwise.|
|name|String|The calendar name.|
|owner|[emailAddress](emailAddress.md)|The email address of the owner of the calendar.|

### Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|calendarView|[event](event.md) collection|The calendar view for the calendar. Navigation property. Read-only.|
|events|[event](event.md) collection|The events in the calendar. Navigation property. Read-only.|
|multiValueExtendedProperties|[multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md) collection| The collection of multi-value extended properties defined for the calendar. Read-only. Nullable.|
|singleValueExtendedProperties|[singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md) collection| The collection of single-value extended properties defined for the calendar. Read-only. Nullable.|

### JSON representation

Here is a JSON representation of the resource

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "calendarView",
    "events"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.calendar"
}-->

```json
{
  "changeKey": "string",
  "color": "String",
  "id": "string (identifier)",
  "isDefaultCalendar": "boolean",
  "name": "string"
}

```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "calendar resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
