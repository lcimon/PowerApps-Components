# Calendar Component
This component allows to display a fully customizable calendar in Power Apps Canvas.
Main features are the following:
- Allow or disable multiple dates selection
- Define the first and last date selectable
- Highlight days with events with customizable colors
- Disable dates
- Show or hide weekends
- Specify the first day of week
- Manage translations
- Responsive layout (including font size)

## Examples
![image](Assets/Calendar-Preview.png)

## Properties
Below are the available properties to customize this component:

### Input
| Name | Type | Description | Default |
|---|---|---|---|
|Default Date | DateTime | Default selected date when Select Multiple is off | Today() |
|Default Dates | Table | Default selected dates when Select Multiple is on | Table({Date: Today()}) |
|Start Date | DateTime | Define the first selectable date | Today() - 365 |
|End Date | DateTime | Define the last selectable date | Today() + 365 |
|Events | Table | Set events items | Table({Date: Today(), Color: Red}, {Date: Today()+1, Color: Green}) |
|Disabled Dates | Table | Define disabled dates | Table({Date:Date(Year(Today()),Month(Today()),25)}) |
|Start Of Week | Number | Define the start of the week | StartOfWeek.Monday |
|Show Weekends | Color | If yes, weekends are shown, else they are hidden | true |
|Color | Color | Set text color | RGBA(0, 0, 0, 1) |
|Selected Color | Color | Set color text of selected days | RGBA(255, 255, 255, 1) |
|Selected Fill | Color | Set background color of selected days | RGBA(48,102,190,1) |
|Disabled Color | Color | Set text color of disabled days | RGBA(186,186,186,1) |
|Disabled Fill | Color | Set background color of disabled days | RGBA(241,241,241,1) |
|Chevron Color | Color | Set chevron color | RGBA(48,102,190,1) |
|Header Color | Color | Set text color of header | RGBA(255, 255, 255, 1) |
|Header Fill | Color | Set background color of header | RGBA(48,102,190,1) |
|Calendar Fill | Color | Set background color of calendar | RGBA(255, 255, 255, 1) |
|Font | Color | Set the font | Font.'Open Sans' |
|Translations | Table | Set list of translated texts | Table({Key: "lblMonday", LocalizedValue: "Mon"}, ...) |

### Behavior
| Name  | Description | Parameters |
|---|---|---|
|OnSelect| Raised when a date is selected | SelectedDate - The date selected by user<br/>HasEvent - Flag to indicate if the date has an event |

### Output
| Name | Type | Description |
|---|---|---|
|Selected Date | DateTime | Return the selected date |
|Selected Dates | Table | Return the selected dates |
|Component ID | Text | Instance component ID |

## Note
This component get inspired by other calendars made by:
* [April Dunnam](https://twitter.com/aprildunnam)
* [Th??ophile CHIN-IN](https://twitter.com/tchinnin)
* [Microsoft](https://powerapps.microsoft.com/fr-fr/blog/powerapps-ten-reusable-components/)

Thanks to them!