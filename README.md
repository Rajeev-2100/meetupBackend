# Meetup Management API

<<<<<<< HEAD
A RESTful API built with Node.js, Express.js, MongoDB, and Mongoose for managing meetup events. This API allows users to create meetup events, retrieve all meetups, search meetups by title, and fetch meetup details by ID.

---
=======
A RESTful API built with **Node.js**, **Express.js**, **MongoDB**, and **Mongoose** to manage meetup events. This project allows users to create meetup events, retrieve all events, fetch events by title, and get event details using the meetup ID.
>>>>>>> 32c70624f174ab2623b5e87b2fae94852a21714d

## Features

* Create a new meetup event
* Retrieve all meetup events
<<<<<<< HEAD
* Retrieve meetup details by title
* Retrieve meetup details by ID
* MongoDB integration using Mongoose
* Environment variable support with dotenv
* CORS enabled for frontend integration
* Structured schema validation using Mongoose
=======
* Retrieve meetup details by event title
* Retrieve meetup details by meetup ID
* MongoDB database integration using Mongoose
* CORS enabled for frontend integration
* Environment variable support using dotenv
>>>>>>> 32c70624f174ab2623b5e87b2fae94852a21714d

---

## Tech Stack

* Node.js
* Express.js
* MongoDB
* Mongoose
* dotenv
* cors

---

## Installation

### Clone the Repository

```bash
<<<<<<< HEAD
git clone https://github.com/Rajeev-2100/meetupBackend.git
cd meetupBackend
=======
git clone https://github.com/Rajeev-2100/meetupBackend
cd meetup-api
>>>>>>> 32c70624f174ab2623b5e87b2fae94852a21714d
```

### Install Dependencies

```bash
npm install
```

### Create Environment Variables

<<<<<<< HEAD
Create a `.env` file in the project root.
=======
Create a `.env` file in the root directory.
>>>>>>> 32c70624f174ab2623b5e87b2fae94852a21714d

```env
MONGO_URL=your_mongodb_connection_string
```

### Run the Server

```bash
node index.js
```

<<<<<<< HEAD
Server will start on:
=======
The server will start on:
>>>>>>> 32c70624f174ab2623b5e87b2fae94852a21714d

```bash
http://localhost:3001
```

---

<<<<<<< HEAD
## Project Structure

```bash
├── db
│   └── db.connect.js
│
├── model
│   └── meetup.model.js
│
├── .env
├── index.js
├── package.json
└── README.md
```

---

## Meetup Schema
=======
## Database Schema

### Meetup Model
>>>>>>> 32c70624f174ab2623b5e87b2fae94852a21714d

| Field           | Type   | Required |
| --------------- | ------ | -------- |
| eventTitle      | String | Yes      |
| hostedBy        | String | Yes      |
| imageUrl        | String | Yes      |
| eventDetail     | String | Yes      |
| dressCode       | Array  | Yes      |
| ageRestrictions | Number | Yes      |
| eventTags       | Array  | Yes      |
| eventDate       | Date   | Yes      |
| eventLocation   | String | Yes      |
| eventPrice      | Number | Yes      |
| noOfSpeaker     | Number | Yes      |
| speakerPerson   | String | Yes      |
| speakerRole     | Array  | Yes      |
| eventType       | Array  | Yes      |

<<<<<<< HEAD
### Allowed Dress Codes

```js
["Smart casual", "Formal", "Informal"]
```

### Allowed Event Tags

```js
["marketing", "digital", "technical"]
```

### Allowed Speaker Roles
=======
### Allowed Values

#### Dress Code

```js
[
  "Smart casual",
  "Formal",
  "Informal"
]
```

#### Event Tags

```js
[
  "marketing",
  "digital",
  "technical"
]
```

#### Speaker Roles
>>>>>>> 32c70624f174ab2623b5e87b2fae94852a21714d

```js
[
  "Marketing Manager",
  "SEO Specialist",
  "Developer"
]
```

<<<<<<< HEAD
### Allowed Event Types
=======
#### Event Types
>>>>>>> 32c70624f174ab2623b5e87b2fae94852a21714d

```js
[
  "Offline Event",
  "Online Event"
]
```

---

## API Endpoints

### Create Meetup

**POST /**

Creates a new meetup event.

#### Request Body

```json
{
  "eventTitle": "React Meetup 2026",
  "hostedBy": "Tech Community",
  "imageUrl": "https://example.com/image.jpg",
  "eventDetail": "A meetup for React developers.",
  "dressCode": ["Smart casual"],
  "ageRestrictions": 18,
  "eventTags": ["technical"],
  "eventDate": "2026-06-20",
  "eventLocation": "Delhi",
  "eventPrice": 499,
  "noOfSpeaker": 2,
  "speakerPerson": "Rajeev Rawat",
  "speakerRole": ["Developer"],
  "eventType": ["Offline Event"]
}
```

<<<<<<< HEAD
#### Success Response

```json
{
  "message": "Meetup Data upload successfully",
  "data": {}
=======
#### Response

```json
{
  "message": "Meetup Data upload successfully"
>>>>>>> 32c70624f174ab2623b5e87b2fae94852a21714d
}
```

---

### Get All Meetups

**GET /meetup**

Returns all meetup events.

<<<<<<< HEAD
#### Success Response
=======
#### Response
>>>>>>> 32c70624f174ab2623b5e87b2fae94852a21714d

```json
{
  "message": "All meetup data is this:",
  "data": []
}
```

---

### Get Meetup By Title

**GET /meetup/:meetupTitle**

<<<<<<< HEAD
Retrieves meetup details using the meetup title.
=======
Returns meetup details by title.
>>>>>>> 32c70624f174ab2623b5e87b2fae94852a21714d

#### Example

```bash
GET /meetup/React Meetup 2026
```

<<<<<<< HEAD
#### Success Response
=======
#### Response
>>>>>>> 32c70624f174ab2623b5e87b2fae94852a21714d

```json
{
  "message": "Meetup Data upload successfully",
  "data": {}
}
```

---

### Get Meetup By ID

<<<<<<< HEAD
**GET /meetup/id/:meetupId**

Retrieves meetup details using the MongoDB document ID.
=======
**GET /meetup/Id/:meetupId**

Returns meetup details using MongoDB document ID.
>>>>>>> 32c70624f174ab2623b5e87b2fae94852a21714d

#### Example

```bash
<<<<<<< HEAD
GET /meetup/id/6842d1c0bdf4e3a7d91e1234
```

#### Success Response
=======
GET /meetup/Id/6842d1c0bdf4e3a7d91e1234
```

#### Response
>>>>>>> 32c70624f174ab2623b5e87b2fae94852a21714d

```json
{
  "message": "Meetup Data upload successfully",
  "data": {}
}
```

---

<<<<<<< HEAD
## Database Connection

The application connects to MongoDB using Mongoose.

```js
mongoose.connect(process.env.MONGO_URL)
```

Environment variables are managed using dotenv.

=======
## Project Structure

```bash
├── db
│   └── db.connect.js
│
├── model
│   └── meetup.model.js
│
├── .env
├── index.js
├── package.json
└── README.md
```

>>>>>>> 32c70624f174ab2623b5e87b2fae94852a21714d
---

## Learning Outcomes

Through this project, I learned:

<<<<<<< HEAD
* Building REST APIs with Express.js
* Connecting MongoDB using Mongoose
* Designing schemas and validations
* Working with async/await
* Managing environment variables using dotenv
* Structuring backend applications
* Handling HTTP requests and responses
* Implementing API endpoints
* Database querying with Mongoose
=======
* Creating REST APIs using Express.js
* Connecting MongoDB with Mongoose
* Designing schemas and validations
* Using async/await for database operations
* Managing environment variables with dotenv
* Structuring backend applications
* Handling HTTP requests and responses
* Implementing CRUD-related API endpoints
* Error handling in Express applications
>>>>>>> 32c70624f174ab2623b5e87b2fae94852a21714d
* Testing APIs using Postman

---

## Future Improvements

* Update meetup details
* Delete meetup events
* Pagination support
<<<<<<< HEAD
* Search and filtering
* Authentication and authorization
* Image uploads using Cloudinary
=======
* Search and filter meetups
* Authentication and authorization
* Image upload support using Cloudinary
>>>>>>> 32c70624f174ab2623b5e87b2fae94852a21714d
* Event registration functionality

---

## Author

Rajeev Rawat

Backend project built using Node.js, Express.js, MongoDB, and Mongoose for managing meetup event data.
<<<<<<< HEAD

GitHub: https://github.com/Rajeev-2100

---

## License

This project is licensed under the MIT License.
=======
>>>>>>> 32c70624f174ab2623b5e87b2fae94852a21714d
