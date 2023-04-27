# meet

The "meet" app is an app where you can search for upcoming events in different cities at different times. 

_______________________________________________________________________________________________________________________________________________________________________

Feature 1: Filter eventy by city

SCENARIO 1: WHEN USER HASN’T SEARCHED FOR A CITY, SHOW UPCOMING EVENTS FROM ALL CITIES.
Given user hasn’t searched for any city
When the user opens the app
Then the user should see a list of all upcoming events

SCENARIO 2: USER SHOULD SEE A LIST OF SUGGESTIONS WHEN THEY SEARCH FOR A CITY.
Given the main page is open
When user starts typing in the city textbox
Then the user should see a list of cities (suggestions) that match what they’ve typed

SCENARIO 3: USER CAN SELECT A CITY FROM THE SUGGESTED LIST.
Given the user was typing “Berlin” in the city textbox
And the list of suggested cities is showing
When the user selects a city (e.g., “Berlin, Germany”) from the list
Then their city should be changed to that city (i.e., “Berlin, Germany”)
And the user should receive a list of upcoming events in that city

Feature 2: Show/hide event's details

SCENARIO 1: AN EVENT ELEMENT IS COLLAPSED BY DEFAULT
Given data has been loaded
When user looks at a list of events
Then the event's details will not be visible

SCENARIO 2: USER CAN EXPAND AN EVENT TO SEE ITS DETAILS
Given a list of events is shown
When user clicks a button
Then the events details will be shown

SCENARIO 3: USER CAN COLLAPSE AN EVENT TO HIDE ITS DETAILS
Given an events details are shown
When user clicks a button
Then the events details will be hidden

Feature 3: Specify number of events

SCENARIO 1: WHEN USER HASN'T SPECIFIED A NUMBER; 32 IS THE DEFAULT NUMBER
Given a list of events is shown
When the user hasn't specified a number
Then 32 events will be shown

SCENARIO 2: USER CAN CHANGE THE NUMBER OF EVENTS THEY WANT TO SEE
Given the user hasn't specified a number
When he specifies a number
Then as many events as he wishes will be shown

Feature 4: Use the app when offline

SCENARIO 1: SHOW CACHED DATA WHEN THERE'S NO INTERNET CONNECTION
Given there's no internet connection
When user uses the app
Then cached data will be shown

SCENARIO 2: SHOW ERROR WHEN USER CHANGES THE SETTINGS (CITY, TIME RANGE)
Given user uses the app offline
When user changes settings like city or time range
Then an error message will be shown

Feature 5: Data visualization

SCENARIO 1: SHOW A CHART WITH THE NUMBER OF UPCOMING EVENTS IN EACH CITY
Given the user is looking for events
When the user chooses a city
Then a chart with the number of upcoming events in that city will be shown


