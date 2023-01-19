# R1 Description of your website, including

- Purpose

This app will provide a way for people to exchange books, find out about new books and obtain a new book to read without having to pay.

- Functionality / features

  1. MVP features are:
      - General users can view the list of the books available or pending for exchange.
      - General users can view the details of each book.
      - General users can search books by category (e.g. author, title, language, genre, etc.) or by location.
      - General users can make an appointment for book exchange with their preferred time and the details of their own book to be exchanged.
      - The books' status can be updated automatically to pending once one appointment is made on it.

  2. Advanced features are:
       - Admin can update the status of the exchanged book to available again or confirm the sucess of the exchange.
       - General users can view/edit their appointment.
       - General users can view their own profile.
       - General users can view their book list.

- Target audience

This app is designed and developed for a voluntary community of readers or book lovers or those who would like to share their loved books with others. 

- Tech stack
  
  - MongoDB
  - Mongoose
  - Express
  - React
  - Node
  - HTML
  - CSS
  - Jest
  - Vitest
  - Supertest
  - Cors
  - Vite

# R2 Dataflow Diagram

![Dataflow Diagram](docs/Data%20Flow%202.png)

# R3 Application Architecture Diagram

![AAD](./docs/AAD-Book%20Exchange.png)

1. The web browser that the user interacts with directly. The user can access the server by using different devices such as mobile, tablet and laptop etc,. This is the only section that the user directly uses, because the browser will send the request and receive the response from the Front-end and display it.

2. This part is written in React, CSS, JavaScript and HTML. It is represented as a  Front-end by receiving the HTTP request from the users and it will receive the data and function by sending the JSON request to the back-end. Once it receives the response from the back-end then the front-end can send the render to the browser by a HTTP response.
In the Front-End, there are five components which are Home, Books, Appointment, Confirmation and Contact, and each component will send the JSON request to the Back-End for getting the data to display to the web browser.
Besides, in the Home component, it is linking to Books and Appointments component by using the 'Display books' function. Also, the Appointment component is linking to Confirmation component since the user submitted the appointment from.
Moreover, it may get tested and deployed by using the Railway.

3. This part is a Back-End by using Express.js, Node.js and JavaScript. It is for receiving the JSON request from the Front-End and then it will match the URL first and ask the MongoDB database to query the data that the server needs and then will send the response back to the Front-End. Each API may receive different requests from different components based on the functionalities  and features.
For example, the Books API will receive the request to GET(display) the data of the books details and then it will match and query the database to get the data.
In the Appointment API which will receive a request to POST(create) a new book, PUT(update) the selected book details and POST(create) a new appointment to store to the database.
In the Location API, some of the components will request to GET (display) the data of the location details from the database and get back to the Front-End. 
Moreover, it may get tested and deployed by using the Railway.

4. This part is a database by using MongoDB Atlas. The database mainly has three tables to store different type of data which is Books, Appointments and Locations.The database will receive the queries from the Back-End by using mongoose and then the Back-End can store, retrieve and edit the data from the database and send the latest data back to the Back-End.

# R4 User Stories

In general, 

- As readers (i.e. general users), they want to know if there are any books that they are interested in and available for exchange around their area, so that they can use their own books to exchange.
- As readers (i.e. general users), they want to know the details of the books available for exchange, so that they can decide to exchange or not.
- As redears (i.e. general users), they want to select a book from the app to exchange with their own book.
- As readers (i.e. general users), they want to make an appointment for exchange, so that they can make an arrangement.
- As readers (i.e. general users), they want to know the status of their preferred book, so that they can tell if an exchange is available for that book.

Furthermore,

- As readers (i.e. general users), they want to view their appointments, so that they can set up a reminder.
- As readers (i.e. general users), they want to edit their appointments, so that they can make an amendment if something unexpected happens.
- As readers (i.e. general users), they want to view the list of books they have exchanged, so that they can have a record.
- As admins, they want to edit the status of the pending books, so that the readers can be updated in time about the exchange.

# R5 Wireframes for multiple standard screen sizes, created using industry standard software

![Wireframes](docs/Book%20Exchange%20Wireframe.png)

# R6 Screenshots of your Trello board throughout the duration of the project

Day 1 - Tue 17 Jan

![Trello](docs/Trello%20board/Trello%20-17%20Jan.png)

Day 2 - Wed 18 Jan

![Trello](docs/Trello%20board/Trello%20-%2018%20Jan.png)

Day 3 - Thu 19 Jan

![Trello](docs/Trello%20board/Trello%20-%2018%20Jan%20-%202.png)