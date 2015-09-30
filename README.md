# Floraful
![] (http://i.imgur.com/wBcUl2j.png)

## Floraful is a web application to allow users to input plant observations and to provide output reports of the observed data

## TABLE OF CONTENTS
---------------------
   
### [Introduction] (#a1)
### [Database Outline] (#a2)
### [Form Outline] (#a3)
### [Client-side Outline] (#a4)
### [Optional Features] (#a5)
### [Maintainers] (#a6)

<a name="a1"/>
## INTRODUCTION
------------
The purpose of this application is to gather information on local flora in the state of Colorado via user-submitted data, with an emphasis on ease of use for the end-user submitting information through the use of a form on a responsive site, most likely on a smartphone in the field. Flora is defined as the plants of a particular region, habitat, or geologic period. For this database, flora is defined
as plants currently found growing in the state of Colorado. The information gathered includes an optional name of the user, a unique non-sequential identifier for the record, a timestamp, name of the plant, soil conditions, weather conditions, location, and a notes field for any other relevant information. This website and database are being used to gather a current status of the Flora in Colorado, as well as to detect changes in the flora over time.

A privileged user will then have access to the database through a password-protected login and be able to view the information in a browser, with the option to download the information in a user-generated report form (CSV file) that can then be imported into a Microsoft Excel spreadsheet. This user will  be able to add users and edit entries. The end-user will not have access to this information, but rather a user with administrative privileges. 

<a name="a2"/>
## DATABASE OUTLINE
-------------
| Field              | Data Type    |
|--------------------|--------------|
| Observer Name      | VARCHAR(50)  |
| Unique Identifier  | INT          |
| Name of Plant      | VARCHAR(100) |
| Soil Conditions    | ARRAY        |
| Weather Conditions | VARCHAR(50)  |
| Date/Time          | TIMESTAMP    |
| Location           | VARCHAR(50)  |
| Notes              | VARCHAR(200) |

<a name="a3"/>
## FORM OUTLINE
-------------
|Field               | Form Field |
|--------------------|------------|
| Observer Name      | text       |
| Unique Identifier  | hidden     |
| Name of Plant      | text       |
| Soil Conditions    | select     |
| Weather Conditions | text       |
| Date/Time          | datetime   |
| Location           |  text      |
| Notes              | textarea   |
| Submit             | submit     |

<a name="a4"/>
## CLIENT-SIDE OUTLINE   [Floraful.com]


Welcome to Floraful.
You may enter as many Plants from as many locations as you like.  The Plants entered must be planted in the ground and
be growing outside.  They may be perennials or annuals.

### DATA FIELDS

Each data field to have an explanation of what data is to be entered in that field, either on the web page and/or in a
hover text box.

1.  Plant Name  *[Enter the name of the Plant, if known.  Otherwise enter a brief description of the Plant.]*
    - Text Box
    - Datatype is TBD
    - Optional Feature - Attach a picture of the Plant.

2.  Soil Conditions  *[Enter any combination of Clay, Loam, Peat, Rocky, Sand, or Silt descriptors as well
    as Soil Color.]*
    - Text Box
    - Datatype is TBD

3.  Weather Conditions  *[Enter the weather conditions while observing the Plant.  Enter any combination
    of Sunny, Partly Sunny, Cloudy, Raining, Snowing, Fog, Misting, Windy, etc.  Also enter an estimate of
    the Temperature.]*
    - Text Box
    - Datatype is TBD

4.  Location  *[Enter the location where the Plant was seen.]*
    - Text Box
    - Datatype is TBD
    - Optional Feature - Gather the Latitude and Longitude from the GPS sensor on the recording device.

5.  Name of the person entering the record.  *[Enter your First and Last Name.]*
    - Text Box
    - Datatype is TBD

6.  Additional Notes     *[Add any additional notes and observations.]*
    - Text Box
    - Datatype is TBD

7.  Date and Time the record was submitted.  Not seen by user while entering data.
    - From the server time stamp.
    - Datatype is TBD

### BUTTONS

1.  Submit Button

    Checks that all user entered fields contain valid data.  If not, then returns the user to the Main Page
      with the missing data field(s) highlighted in red.  If correct, goes to Data Submitted Page.


### DATA SUBMITTED PAGE    [Floraful.com/thankyou]


Thank you (Name of person entering the record from Main Page) for submitting this Plant data.

Please enter as many Plants as you wish.

- Optional Feature - Button to Enter another plant.

### BUTTONS

1.  Enter Another Plant Button
    
    Return to Main Page but keep the person's Name, Soil Conditions, Weather Conditions, and Location
      fields.



### **REPORT PASSWORD PAGE**     [Floraful.com/report]

This page allows you to generate a report of all the Flora records currently in the Flora Finders database ordered by
the Date and Time they were entered.

### DATA FIELDS

1.  Password     [To generate the report enter your password.]

    Text Box

Validate password.  If not valid, generate error message and focus cursor on the text box.  If correct, activate the
Generate Report button.

### BUTTONS

1.  Generate Report     [List all items in the Flora database sorted by date and time entered.]
    - button to generate report on screen
    - Optional Feature - button to create pdf report.
    
<a name="a5"/> 
## OPTIONAL FEATURES
-----------
- access weather api to gather weather conditions when observation is taken.
- access geocoding api to get latitude and longitude of location when observation is taken.

<a name="a6"/>   
## MAINTAINERS
-----------
### Current maintainers:
* Mark Newcomb - https://github.com/MarkNewcomb1
* Steve Krog - https://github.com/stevekrog
* Rick Lamp - https://github.com/ricklamp5

----------------------
This project has been sponsored by:
 * Weblab Backend Development Boot Camp
