# Meetup Management API

A RESTful API built with Node.js, Express.js, MongoDB, and Mongoose for managing meetup events. This API allows users to create meetup events, retrieve all meetups, search meetups by title, and fetch meetup details by ID.

---

## Features

* Create a new meetup event
* Retrieve all meetup events
* Retrieve meetup details by title
* Retrieve meetup details by ID
* MongoDB integration using Mongoose
* Environment variable support with dotenv
* CORS enabled for frontend integration
* Structured schema validation using Mongoose

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
git clone https://github.com/Rajeev-2100/meetupBackend.git
cd meetupBackend
```

### Install Dependencies

```bash
npm install
```

### Create Environment Variables

Create a `.env` file in the project root.

```env
MONGO_URL=your_mongodb_connection_string
```

### Run the Server

```bash
node index.js
```

Server will start on:

```bash
http://localhost:3001
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

## Meetup Schema

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

### Allowed Dress Codes

```js
["Smart casual", "Formal", "Informal"]
```

### Allowed Event Tags

```js
["marketing", "digital", "technical"]
```

### Allowed Speaker Roles

```js
[
  "Marketing Manager",
  "SEO Specialist",
  "Developer"
]
```

### Allowed Event Types

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

#### Success Response

```json
{
  "message": "Meetup Data upload successfully",
  "data": {}
}
```

---

### Get All Meetups

**GET /meetup**

Returns all meetup events.

#### Success Response

```json
{
  "message": "All meetup data is this:",
  "data": []
}
```

---

### Get Meetup By Title

**GET /meetup/:meetupTitle**

Retrieves meetup details using the meetup title.

#### Example

```bash
GET /meetup/React Meetup 2026
```

#### Success Response

```json
{
  "message": "Meetup Data upload successfully",
  "data": {}
}
```

---

### Get Meetup By ID

**GET /meetup/id/:meetupId**

Retrieves meetup details using the MongoDB document ID.

#### Example

```bash
GET /meetup/id/6842d1c0bdf4e3a7d91e1234
```

#### Success Response

```json
{
  "message": "Meetup Data upload successfully",
  "data": {}
}
```

---

## Database Connection

The application connects to MongoDB using Mongoose.

```js
mongoose.connect(process.env.MONGO_URL)
```

Environment variables are managed using dotenv.

---

## Learning Outcomes

Through this project, I learned:

* Building REST APIs with Express.js
* Connecting MongoDB using Mongoose
* Designing schemas and validations
* Working with async/await
* Managing environment variables using dotenv
* Structuring backend applications
* Handling HTTP requests and responses
* Implementing API endpoints
* Database querying with Mongoose
* Testing APIs using Postman

---

## Future Improvements

* Update meetup details
* Delete meetup events
* Pagination support
* Search and filtering
* Authentication and authorization
* Image uploads using Cloudinary
* Event registration functionality

---

## Author

Rajeev Rawat

Backend project built using Node.js, Express.js, MongoDB, and Mongoose for managing meetup event data.

GitHub: https://github.com/Rajeev-2100

---

## License

This project is licensed under the MIT License.
