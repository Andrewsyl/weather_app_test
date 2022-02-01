# Weather Sensor App

- Full-stack weather app
- App allows users to add sensors based on location.
- Then based on the location, an API call is run in the background to collect real-life data.
- This data is then stored in the apps database.
- The database can then be queried for data to give average temperature, humidity, wind speed etc.

##  Built With

* Python
* Flask
* HTML
* CSS
* SQLite
* Bootstrap
* Javascript

# Installation

Prerequisites:

- Python
- Pip
- Git

1. In a terminal, cd to folder location of your choice
2. Enter
 ```
  git clone https://github.com/Andrewsyl/222.git
  ```
4. cd to 222 folder and enter
```
pip install -r requirements.txt
```
6. To initialise the database:

- run python in the terminal and enter
```
from app import db
```
Then
```
db.create_all()
```
Followed by
```
exit()
```

Once done and still in the 222 folder, run python app.py and open your browser at address http://127.0.0.1:5000

## Reviewing Code

* Main file is app.py. All routing and major functionality is located here.

## Improvements

#### Functionality

* Improve the error handling. Currently there are some handling that flags city + country names. I would add a JSON file with a list of cities to choose from.
* Regarding db Queries 
* 

#### Code

* Separate Models into their own file. As the project grows the app.py file would grow too large to manage.
* Breakup functions in app.py. Some functions are doing multiple jobs. All should have one job (where possible) and given comments to explain said job.
* I added an API Key for gathering external weather data. I would remove this and ask the user to fetch their own Key.

#### Testing

Use assert test for the Models to test data being saved to database is correct. e.g 

sensor = Sensor('Galway', 'Ireland')
assert user.city == 'Galway'
assert user.country != 'Ireland'



* 
    GIVEN - what are the initial conditions for the test?
    WHEN - what is occurring that needs to be tested?
    THEN - what is the expected response?

* Remove redundant code. Some tests are similar and could be combined using a loop.
* Test data being stored in database


