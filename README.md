# Volcanic Eruption Database

## Description
Volcanoes can cause seemingly unpredictable natural disasters and there is not a current, user friendly website that provides the relevant information on volcanoes all in one place. The lack of knowledge of volcanoes not only fuels people's fear but can also cause widespread panic should eruption happen. We built our site to provide information volcanoes, display volcanic data, and allow users to visually view volcanic activity and add volcanic information to our site—all in a user friendly environment.

## Link to Website
https://volcanic-eruptions-database.herokuapp.com/

## Target Browsers
* Most desktop browsers

## Link to Developer Manual
https://github.com/vihtle/INST377-Group3-Project#developer-manual

# Developer Manual
## How to install application and all dependencies
1. Clone this repository through Github Desktop or through Terminal.
2. Open repository in VSCode Terminal or Terminal application.
3. type ```npm install``` into terminal window and run.
4. The application should now be set to use.

## How to run application on a server
1. Open repository in VSCode terminal or Terminal application.
2. Run ```npm start```. There should be no errors.
3. In a web browser, go to url: ```http://localhost:3000/```.

## To run tests for software
There are no prewritten tests in the source repository currently
1. Open two terminals and make sure you are in the main project directory
2. In the first terminal, run ```npm start```.
3. In the second terminal run ```npm test```.

## API Server Endpoints
  ```/api/eruption_aoa``` - API route for AOA (Area of Activity)
  * GET - Returns data from a SELECT statement of the AOA table as a JSON response along with a message to the console
  * POST - Updates the data based on aoa_id
  * PUT - Inserts data where id is auto incremented
  * DELETE - Deletes data based on aoa_id

  ```/api/eruption_category``` - API route for eruption category
  * GET - Returns data from a SELECT statement of the eruption_category table as a JSON response along with a message to the console
  * POST - Updates the data based on category_id
  * PUT - Inserts data where id is auto incremented
  
   ```/api/eruption_info``` - API route for eruption informations
  * GET - Returns data from a SELECT statement of the eruption_info table as a JSON response along with a message to the console
  * POST - Updates the data based on eruption_id
  * PUT - Inserts data where id is auto incremented
  * DELETE - Deletes data based on eruption_id
  
  `/api/evidence` - API route for evidence data and methods.
  * GET - Returns the data from the json response with SELECT statements EvidenceController.js
  * POST - Updates the data using the Evidence id through joins.
  * PUT - inserts the data into the data columns based on the evidence id given.
  * DELETE - deletes the rows using evidence id as a conditional statement.

  `/api/vei` - API route for vei (Volcanic Explosivity Index).
  * GET - Returns data from a SELECT statement of the vei table as a JSON response along with a message to the console.
  * POST - Updates the data based on vei_id.
  * PUT - inserts the data into the data columns based on the vei_id given.
  * DELETE - Deletes data based on vei_id.

  `/api/volcanos_has_references_table` - API route for volcanos_has_references_table
  * GET - Returns data from a SELECT statement of the volcanos_has_references_table table as a JSON response along with a message to the console.
  * POST - Works out of order and you have to specifiy topic_id when passing the arguement which should be incremental.
  * PUT - Does not work at all due to some foreign key limition.
  * DELETE - Deletes data from the table based on topic id, but is not very useful because adding data via POST is buggy.
  
  `/api/volcanos` - API route for volcanos table
  * GET - Returns data from a SELECT statement of the volcanos table as a JSON response along with a message to the console.
  * POST - Updates the data based on volcano_id
  * PUT - Inserts data where id is auto incremented
  * DELETE - Deletes data based on volcano_id

`/api/eruption_freq` - API route for eruptions per year
  * GET - Returns data from a SELECT statement of the count of eruptions per year

`/api/category_freq` - API route for confirmed eruptions per month
  * GET - Returns data with the json response from a SELECT statement of the count of confirmed eruptions per month



  
## Known Bugs and Future Development
### Bugs:
- Null/blank values in Eruption AOA and Eruption Category that needs to be handled
- Delete for Edit Volcanoes doesn't work. If you'd like a volcano to not appear on the page, delete all of the eruptions. The volcano itself must be deleted through SQL.
- Page currently only loads on mouse move
- Form submission page shows up even if submission failed
- Find use for all the tables in the database because some are only used to reference other tables and do not have much useful information

### Future Development: 
* Add educational information regarding volcanoes.
* Adding more informational charts.
* Adding more volcanos and eruptions, goal is to have a complete database
* Add an advanced search option with filters
* Paginate the home page - We had the html working for this using bulma, but could not figure out the javascript to make the buttons work. 
