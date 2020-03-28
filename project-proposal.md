# Zodiac Sign Analysis Program
### X-Team 208

#### By: Ethan Sun, Prafull Sharma, Spencer Schoenberg, and Theodore Nguyen

## PROBLEM:

## PRIMARY STAKEHOLDER:	

## GUI SKETCHES:

The GUI would have the following structure: 

- main menu
	- textbox inputs for month/day/year
	- yes or no button to proceed with finding zodiac sign
- input zodiac file menu
	- textbox for filename and error handling
- save output to file menu
	- same as above

## DATA STRUCTURES:
For the functionality of this program, the String names of as well as the corresponding amount of days in each month will need to be recorded and internally stored. For this reason, it would make the most sense to store this information in the form of multiple arrays. These arrays (for month name, days in each month) would be used to check the validity of the user’s program input. Comparing user input to the contents of these arrays will ensure that the user has not entered a date that is too far into the future or the past, and that the entered month is between January and December. Leap years will be accounted for by checking if the entered year is divisible by 4 with no remainder, and if this is true, the number of days in the month of February will be increased to 29 in the event that the user’s date of birth is 2/29/… There would also need to be another array (of type String) for the corresponding zodiac signs of each month. This array will be formatted in parallel to the array containing month names, so that a single index will refer to the correct month as well as the proper zodiac sign on both arrays.

As users continue to create inputs on our program, we will have a running list in which we log the results of different inputs with the user’s name and zodiac sign. A hashtable would be ideal for this implementation so that after users have completed their tests, a list of people with the same zodiac sign from the hashtable will be displayed back.

INPUT DATA FILE FORMAT:
The Input Data File Format could be in JSON, with the keys being the user’s first and last name and date of birth (month, day, year) If this file is uploaded, it’s contents would be read and a zodiac sign would be calculated. Then, this new object would be properly hashed and stored in the aforementioned hashtable. An example of a JSON file to upload would be this:

```json
 {
           "firstName": "John",
           "lastName": "Smith",
           "birthday": {
               "month": "June",
               "date": "8",
               "year": "1990"
           }
 }
```
An addition input file would store the correct dates for each Zodiac and information about each sign including start and end date (in day index of the year)

```json
{
    "signs": [
        {
            "name": "Leo",
            "range": {
                "begin": 0,
                "end": 53
            },
            "info": "The Leo Zodiac says ...."
        }
    ]
}
```
## OUTPUT EXAMPLE:
```
John Smith used Zodiac Sign Analysis and found out their sign is Leo. The Leo Zodiac says .... 
```

## MILESTONES:

- Get functionality of zodiac calculator in console only
- Get zodiac json import from JSON file
- Get output to print to file
- Get GUI for each menu type
	- Main Menu
	- Input Zodiac JSON file Menu
	- Output file save Menu

## ASSIGN TASKS: