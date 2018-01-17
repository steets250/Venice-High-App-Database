# Venice High App Data

The following are explanations for each of the fields used for the app data. It's best to edit the JSON files directly for small changes, and only edit and create a CSV file for a larger number of edits.

## Buildings
* name - Name of the building.
* latitude - Latitude coordinate from iOS map data.
* longitude - Longitude coordinate from iOS map data.

## Dates
* yy - Four digit year.
* mm - One or two digit month. Don't include 0 for single-digit months.
* dd - One or two digit day. Don't include 0 for single-digit days.
* s - Schedule number. Refer to the schedules file in the Times folder.

## Events
* title - Title of the event.
* link - Optional URL of the event.
* startDate - Beginning of event. Must be in the format mm/dd/yy.
* endDate - End of event, can be same day as beginning. Must be in the format mm/dd/yy.
* startTime - Start time of event. Must be in the format hh:mm AA. AA can be either am or pm.
* endTime - End time of event. Must be in the format hh:mm AA. AA can be either am or pm.

## Rooms
* number - Room number. Use abbreviation for longer names (e.g. EGYM for east gym).
* building - Must exactly match one building from the buildings list.
* floor - Floor number, either blank, 1, or 2.
* altid - Longer room name, used for shops and rooms without a number.

## Staff
* id - First two letters of first name and last name.
* prefix - Mr., Ms., or Dr.
* firstName - Staff's first name.
* lastName - Staff's last name.
* email - Staff's full email address.
* link - From [this page](https://venicehs-lausd-ca.schoolloop.com/cms/page_view?d=x&piid=&vpid=1445756245343). Right click on a staff's link to get group id.
* mata, sma, wlgs, alps, stemm - Status of magnet membership.
* p0, p1, p2, p3, p4, p5, p6, p7 - Must exactly match a room, or be CONF, /, WASC, UTLA, or RSP.

## Times
### Schedules
* id - Order that the schedules should in the bell schedule page.
* file - The matching filename for each schedule.
* title - Title of the schedule. WIll be displayed in the bell page and widget.
* Follow the format outlined below to create and edit the schedule files.

### Individual Schedules
* id - Periods should be p and the number. Nutrition=n and lunch=l. Passing period should be pp and the number of the upcoming period.
* sh - Starting hour. Should not start with a 0.
* sm - Starting minute. Should not start with a 0, but can be 0.
* eh - Ending hour. Should not start with a 0.
* em - Ending minute. Should not start with a 0, but can be 0.
* title - Title shown in the widget. Should be name of period or passing message.

## Year
* name - Either "start" or "end".
* yy - Four digit year.
* mm - One or two digit month. Don't include 0 for single-digit months.
* dd - One or two digit day. Don't include 0 for single-digit days.

## CSV to JSON
[Convert CSV to JSON](http://www.convertcsv.com/csv-to-json.htm)

Use the following link to convert edited CSV files into JSON.
For step 2, check off the "First row is column names" box.
Once converted, the files should be checked for null values. Any occurrences of null should be replaced with an empty set of double quotes ("").
Commit the uploaded file to [GitHub](https://github.com/steets250/Venice-High-App-Data), and then the app will use the new data the next time it is run.
