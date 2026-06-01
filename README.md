# Meetup Management API

A RESTful API built with **Node.js**, **Express.js**, **MongoDB**, and **Mongoose** to manage meetup events. This project allows users to create meetup events, retrieve all events, fetch events by title, and get event details using the meetup ID.

## Features

* Create a new meetup event
* Retrieve all meetup events
* Retrieve meetup details by event title
* Retrieve meetup details by meetup ID
* MongoDB database integration using Mongoose
* CORS enabled for frontend integration
* Environment variable support using dotenv

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
git clone <repository-url>
cd meetup-api
```

### Install Dependencies

```bash
npm install
```

### Create Environment Variables

Create a `.env` file in the root directory.

```env
MONGO_URL=your_mongodb_connection_string
```

### Run the Server

```bash
node index.js
```

The server will start on:

```bash
http://localhost:3001
```

---

## Database Schema

### Meetup Model

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

```js
[
  "Marketing Manager",
  "SEO Specialist",
  "Developer"
]
```

#### Event Types

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

#### Response

```json
{
  "message": "Meetup Data upload successfully"
}
```

---

### Get All Meetups

**GET /meetup**

Returns all meetup events.

#### Response

```json
{
  "message": "All meetup data is this:",
  "data": []
}
```

---

### Get Meetup By Title

**GET /meetup/:meetupTitle**

Returns meetup details by title.

#### Example

```bash
GET /meetup/React Meetup 2026
```

#### Response

```json
{
  "message": "Meetup Data upload successfully",
  "data": {}
}
```

---

### Get Meetup By ID

**GET /meetup/Id/:meetupId**

Returns meetup details using MongoDB document ID.

#### Example

```bash
GET /meetup/Id/6842d1c0bdf4e3a7d91e1234
```

#### Response

```json
{
  "message": "Meetup Data upload successfully",
  "data": {}
}
```

---

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

## Learning Outcomes

Through this project, I learned:

* Creating REST APIs using Express.js
* Connecting MongoDB with Mongoose
* Designing schemas and validations
* Using async/await for database operations
* Managing environment variables with dotenv
* Structuring backend applications
* Handling HTTP requests and responses
* Implementing CRUD-related API endpoints
* Error handling in Express applications
* Testing APIs using Postman

---

## Future Improvements

* Update meetup details
* Delete meetup events
* Pagination support
* Search and filter meetups
* Authentication and authorization
* Image upload support using Cloudinary
* Event registration functionality

---

## Author

Rajeev Rawat

Backend project built using Node.js, Express.js, MongoDB, and Mongoose for managing meetup event data.
