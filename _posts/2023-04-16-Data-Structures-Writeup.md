---
layout: post
title: Data Structures Writeup
type: tangibles
courses: { compsci: {week: 14} }
comments: true
---
# Collections

Blog Python Model code and SQLite Database.

- From VSCode using SQLite3 Editor, show your unique collection/table in database, display rows and columns in the table of the SQLite database.

![Alt text](/Nighthawk-Pages/images/table.png)

- From VSCode model, show your unique code that was created to initialize table and create test data.

![Alt text](/Nighthawk-Pages/images/init.png)


# APIs and JSON


- In VSCode, show Python API code definition for request and response using GET, POST, UPDATE methods.


GET

![Alt text](/Nighthawk-Pages/images/g.png)


POST

![Alt text](/Nighthawk-Pages/images/pg.png)



UPDATE
![Alt text](/Nighthawk-Pages/images/p.png)




Discuss algorithmic condition used to direct request to appropriate Python method based on request method.


In this Flask main.py file, the @app.route() decorator defines the URL route ("/") and the allowed request methods (methods=['GET', 'POST', 'PUT']). Inside the view function, handle_request(), the request.method attribute is used to determine the type of request and execute the corresponding logic.



In VSCode, show algorithmic conditions used to validate data on a POST condition.
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

![Alt text](/Nighthawk-Pages/images/null.png)




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



