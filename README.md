## YELP ME OUT!
##### Java servlet application utilizing a MySQL formatted Yelp! dataset


### Project Description:
Yelp Me Out is a pick-up-and-go web app that build upon the yelp academic database to provide a recommendation service where by users can plan a brief itinerary of places that they need to go within a given day. Our recommendation engine suggests a local business that fits the input criteria of the user and provide them with necessary information, location, as well as directions in a minimalist but relevant and organized format.

### Technology:
Database: MySQL

Backend: Java Servlet, Java, JSP

Front End: HTML & CSS

UI Framework: Twitter Bootstrap


### Feature Set:

1. Flexible address input processing where user can enter a variety of location data, including full address, partial 
address, city, state or even landmarks.

2. Accurate Geocoding via Google Maps Geocoding service.

3. Variable recommendation algorithm that returns different (but all good results that satisfy the user’s criteria) on the 
same set of input.

4. Search and queries based on multiple parameters (categories, distance, popularity, and ratings).

5. Google Static Maps.

6. Google Maps Directions for each location suggested.

7. Data visualization such as charts for aggregate rating data.

8. Auto-completion of user category input to improve UX.

9. Maintain path continuity where by the user’s queried result are organized in a logical order regardless of results of user queries (user queries may return empty set in the middle of a trip – implementation maintains consistency in these cases).

Please read the Project Report document for additional information.

========================================================================================================================

YMO folder contains the following front-end and back-end files

	#################### Address Parser.java ###########################
	Given an input address, call the Google Geocoder service to calculate the longitude and latitude coordinate of the given location

	#################### Business.java ##############################
	JavaBean to create Business objects in servlets to pass onto JSP pages

	################# Distance Calculator.java #########################
	Calculate the travel distance between two locations by foot and car

	################# GoogleMapDirectionLink.java ######################
	Given a source and destination. Map it onto google map service and return a formatted URL

	################## LandingServlet.java ############################
	Servlet that processes form data from the index.html page.
	Was initially used to take user log-in data, but was later scraped.

	#################### PlanningServlet.java ##########################
	Bulk of work and integration performed in this file.
	It tediously gathers various parameter values from planTrip.jsp and processes them.

	#################### RangeCalculator.java ##########################
	Calculate the bounding box given a set of coordinates and a radius

	################ RatingChart.java ######################
	Given the rating to a particular business. 
	Translate it into a bar and output a formatted image URL
	
	################### StaticMapGenerator.java ########################
	Given a set of coordinates. Plot them onto a static google map and output a formatted URL

	##################### YelpDB.java ##########################
	DAO used to query local MySQL instance for data. 
 
	################### bootstrap.css ######################
	CSS file that came with Twitter bootstraps download

	################### Arrow.png ########################
	Image of an arrow

	#################### landingfinal.png ##################
	Front page image

	#################### YMO-Logo.png ##################
	Our logo

	#################### bootstrap.js #####################
	Js file that came with Twitter bootstraps download

	#################### jquery.js #####################
	Js file that came with Twitter bootstraps download

	#################### index.html ####################
	Our landing / front page

	#################### planTrip.jsp ##################
	JSP file that contains various forms and options that the user may select.
	Information from this jsp file is submitted to the PlanningServlet

	################## results.jsp ######################
	Outputs processed data from PlanningServlet

	################### charts4j-1.3.jar ################
	JAR for our chart function

	###################### jstl-1.2.jar #################
	JAR for using JSTL 

	##################### mysql-connector ############
	JAR required for using MySQL

YelpMeOut folder contains the code used to import the Yelp data into our MySQL database.

	#################### ImportBusinesses.java ###############
	Follows the format from the homework assignment for importing data.
	Contains DDL for Business table.
	
	#################### ImportReviews.java ###############
	Follows the format from the homework assignment for importing data.
	Contains DDL for Review table.
	
	#################### ImportUsers.java ###############
	Follows the format from the homework assignment for importing data.
	Contains DDL for User table.
