---
layout: post
title: Data Structures Writeup
type: tangibles
courses: { compsci: {week: 14} }
comments: true
---

For our Data Stuctures project, our team decided to focus on a site that would help users with fitness and well-being. My individual CPT feature is a  tracker that tracks sleep and exercise in a specific  user and  records them in a graphs, allowing users to compare their current performance with past records. 

# Collections

Blog Python Model code and SQLite Database.

- From VSCode using SQLite3 Editor, show your unique collection/table in database, display rows and columns in the table of the SQLite database.


For our "collection", we have a database of users. As you can see in the following image, each user has attributes such as name, UID, role, diary entries, exercise details (duration, date, type), and sleep information (quality, date, hours), which is used for my graphs.  The diary entries for User 1 appear to contain multiple entries separated by "///", indicating multiple diary entries for different days or occasions. Users have different roles, such as "admin" or "user". Admin users have special privileges that users do not-they can update or delete other users. 

![Alt text](/Nighthawk-Pages/images/table1.png)


- From VSCode model, show your unique code that was created to initialize table and create test data.


The following code defines a function initUsers() that initializes sample user data and inserts it into the database. rapped in a try-except block. This is used to catch any exceptions that may occur during the execution of the code inside the block. The try-except block is meant to ensure that the process doesn't stop or break if there any errors. The with app.app_context(): ensures that the application context is properly set up before executing the code inside the block, which is necessary for Flask applications. db.create_all() creates the necessary database tables if they don't already exist. This is typically done using SQLAlchemy, a driver in Flask applications to create tables based on the defined models. users_data is a list containing dictionaries, with each dictionary representing data for a single user. Each dictionary contains attributes such as name, UID, password, role, exercise details, sleep details, and diary entries for each user. Using a for loop, the code iterates over each dictionary in users_data and creates a User object using the data. db.session.add(user) adds each user object to the database, while db.session.commit() commits the changes. In the except block,  if an IntegrityError occurs during the insertion process (e.g., due to a violation of a unique constraint), the code rolls back the changes using db.session.rollback(). It also prints an error message indicating the failure to insert data, allowing our team to easily fix the issue. The function call  initUsers() is main.py, along with other function calls for our other models. 

![Alt text](/Nighthawk-Pages/images/database.png)



# Lists  and Dictionaries

Lists 
Blog Python API code and use of List and Dictionaries.
In VSCode using Debugger, I  show a list as extracted from database as Python objects. I have  two distinct example examples of dictionaries, show Keys/Values using debugger.

From Create Endpoint (Post)

![Alt text](/Nighthawk-Pages/images/cook.png)
![Alt text](/Nighthawk-Pages/images/cook2.png)



The keys and values from the debugger are

"id": The value is 8, which represents the unique identifier or database ID for the user.
"name": The value is "Bella M", indicating the name of the user.
"uid": The value is "testperson", which  represent a unique identifier or username for the user.
"password": The value is "sha256$hWX...", which is  a hashed password for the user. The password is hashed for security reasons.
"exercise": The value is an empty string, indicating that there is no exercise data associated with this user.
"sleep": The value is an empty string, indicating that there is no sleep data associated with this user.
"diary": The value is an empty string, indicating that there are no diary entries associated with this user.


From Get (Getting Exercise Data For Graph)
![Alt text](/Nighthawk-Pages/images/photo.png)
![Alt text](/Nighthawk-Pages/images/get.png)

The keys and values from the debugger are: 
"duration": The value is "5", which represents the duration of the exercise session in minutes.
"exerciseDate": The value is "2024-04-05", which represents the date when the exercise session took place.
"exerciseType": The value is "Running", indicating the type of exercise performed during the session. 



# Frontend

- Blog JavaScript API fetch code and formatting code to display JSON.

- In Chrome inspect, and show the response of JSON objects from fetch of GET, POST, and UPDATE methods.

- GET/UPDATE

Here are my get/update responses from getting exercise data from a specific user and appending it to the new data, essentially using get/update. As you can see, this data is formatted into graphs the user can see so they can track their individual  data. 
![Alt text](/Nighthawk-Pages/images/z.png)


- In the Chrome browser, I show a demo (POST) of obtaining an Array of JSON objects that are formatted into the browser's screen. Once I created a user, the JSON is formatted into a table of users, which are also in the database. 

![Alt text](/Nighthawk-Pages/images/r0.png)

![Alt text](/Nighthawk-Pages/images/r.png)

![Alt text](/Nighthawk-Pages/images/r1.png)



- In JavaScript code, describe fetch and method that obtained the Array of JSON objects.

 Here, I fetched data from a specific user using the UD endpoint, which is the endpoint with a specific user id attached.  I added the old data from the JSON exercise array to the new data the user inputted and sent that to the api. I concatenated two JSON arrays.

![Alt text](/Nighthawk-Pages/images/good.png)


- In JavaScript code, shows code that performs iteration and formatting of data into HTML.

Within the JavaScript section, there's a loop that iterates over the sleep data fetched from the server. This loop iterates over each entry in the sleep data array and calculates the total sleep duration for each day. It also determines the color of the bar in the sleep graph based on the quality of sleep/ and uses a switch /case to designated the color based on the quality. 

![Alt text](/Nighthawk-Pages/images/g1.png)

 After iterating over the sleep data, the code extracts the dates, total sleep hours, and colors from the calculated total duration by day object. It does this using Object.keys(), Object.values(), and map() methods to extract and format the data appropriately for use in the Chart.js chart. Finally, the extracted data is used to create a bar chart using the Chart.js library, where I used an external source for the javascript code. The chart is configured with the labels for sleep dates, the total sleep duration data, and the corresponding colors. This chart is then rendered within the HTML canvas element. 

![Alt text](/Nighthawk-Pages/images/g2.png)

- In the Chrome browser, show a demo (POST or UPDATE) gathering and sending input and receiving a response that show an update. Repeat this demo showing both success and failure.

A POST is used to create a user. If successful, the user is redirected to the login page and added to to table in the update page. 


- Success


Update page before new user is create

![Alt text](/Nighthawk-Pages/images/beforepost.png)
 User is registered, response data is shown  in JSON (user.read() is returned, diary, sleep, and exercise are empty because those fields haven't been entered yet)

![Alt text](/Nighthawk-Pages/images/registration.png)

 User is registered, response data is shown  in JSON (user.read() is returned, diary, sleep, and exercise are empty because those fields haven't been entered yet)

![Alt text](/Nighthawk-Pages/images/afterpost.png)

User is redirected to login page after user logging in is successful. 

![Alt text](/Nighthawk-Pages/images/redirect.png)

 User is registered, response data is shown  in JSON  and formatted into the table.




- Failure

If the uid or password is already taken, an error is thrown in the console and the user is alerted with invalid uid or password.

![Alt text](/Nighthawk-Pages/images/8.png)
![Alt text](/Nighthawk-Pages/images/9.png)


- In JavaScript code, show and describe code that handles success. Describe how code shows success to the user in the Chrome Browser screen.  In JavaScript code, show and describe code that handles failure. Describe how the code shows failure to the user in the Chrome Browser screen.


When post is successful, the user is redirected the login page. When the register is unsunccesful, there is an error alerted the console and alerted to the user/ 

![Alt text](/Nighthawk-Pages/images/fail.png)




# APIs and JSON

- In VSCode, show Python API code definition for request and response using GET, POST, UPDATE methods.


GET
![Alt text](/Nighthawk-Pages/images/g.png)


POST
![Alt text](/Nighthawk-Pages/images/pg.png)


UPDATE
![Alt text](/Nighthawk-Pages/images/p.png)

Discuss algorithmic condition used to direct request to appropriate Python method based on request method.
The classes correspond to certain resource, which all have methods that correspond to CRUD operations (POST, GET, PUT, DELETE). Each class a certain link that cooresponsds to the link that the data is fetched from(either data is fetched or appended or created based on the method)


In VSCode, show algorithmic conditions used to validate data on a POST condition. These ensure that a user exists and that the uid are not required/ 
![Alt text](/Nighthawk-Pages/images/c.png)


In Postman, show URL request and Body requirements for GET, POST, and UPDATE methods. In Postman, show the JSON response data for 200 success conditions on GET, POST, and UPDATE methods.

- GET (token required, admin)
![Alt text](/Nighthawk-Pages/images/getall.png)

- POST

![Alt text](/Nighthawk-Pages/images/pull.png)

- UPDATE (PUT)

![Alt text](/Nighthawk-Pages/images/put1.png)

In Postman, show the JSON response for error for 400 when missing body on a POST request.

![Alt text](/Nighthawk-Pages/images/post.png)


In Postman, show the JSON response for error for 404 when providing an unknown user ID to a UPDATE request.

![Alt text](/Nighthawk-Pages/images/pu.png)




#  Optional/Extra, Algorithm Analysis

- Show algorithms and preparation of data for analysis. This includes cleaning, encoding, and one-hot encoding:

![Alt text](/Nighthawk-Pages/images/one.png)

- Show algorithms and preparation for predictions:

![Alt text](/Nighthawk-Pages/images/two.png)

[Video Demo](https://drive.google.com/file/d/1nsliqhjIZPXC-70gKHR9Io8FGqWRXN5z/view)


- Discuss concepts and understanding of Linear Regression algorithms:


![Alt text](/Nighthawk-Pages/images/logisticregression.png)

- Discuss concepts and understanding of Decision Tree analysis algorithms:

![Alt text](/Nighthawk-Pages/images/tree.png)



