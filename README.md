# SLIDELY-FORMS-APP

## Overview

This is the backend server for the Slidely Form App. It handles API requests for creating, reading, updating, and deleting form submissions, which are stored in a JSON file (`db.json`).

## Technologies Used

- **Node.js:** JavaScript runtime environment.
- **Express.js:** Web framework for Node.js.
- **Body-parser:** Middleware for parsing request bodies.
- **File System (fs):** Node.js module for interacting with the file system.

## Setup

1. **Clone the repository:**
   ```sh
   git clone https://github.com/vedanshi0512/slidely-form-app-backend.git
   cd slidely-form-app-backend

## Install dependencies

```bash
npm install
```
## Start Server

```bash
npm start
```
The server will start on *http://localhost:3000*

# API Endpoints

## 1. Create a new submission

URL: /create

Method: POST

Request Body:
```{
    "name": "string",
    "email": "string",
    "phone": "string",
    "github_link": "string",
    "stopwatch_time": "string"
}
```


Response:
```Copy code
{
    "message": "Submission saved"
}
```
## 2. Read all submissions

URL: /read

Method: GET

Response:
```
[
    {
        "name": "string",
        "email": "string",
        "phone": "string",
        "github_link": "string",
        "stopwatch_time": "string"
    },
    ...
]
```
## 3. Update a submission
URL: /update?index={index}

Method: PUT

Request Body:
```
{
    "name": "string",
    "email": "string",
    "phone": "string",
    "github_link": "string",
    "stopwatch_time": "string"
}
```
Response:
```
{
    "message": "Submission updated"
}
```
## 4. Delete a submission
URL: /delete?index={index}

Method: DELETE

Response:
```
{
    "message": "Submission deleted"
}
```

# File Structure
```
slidely-form-app-backend/
│
├── src/
│   ├── server.ts       # Main server file
│   └── db.json         # JSON file to store submissions
│
├── package.json        # Node.js dependencies and scripts
├── README.md           # Documentation
└── tsconfig.json       # TypeScript configuration
```

# Flowchart

Below is the flowchart illustrating the flow of the backend application:

```mermaid
[Client Request] --> [API Endpoint]
    |-- POST /create --> [Read db.json] --> [Add Submission] --> [Write to db.json] --> [Response]
    |-- GET /read --> [Read db.json] --> [Send Submissions] --> [Response]
    |-- PUT /update?index={index} --> [Read db.json] --> [Update Submission] --> [Write to db.json] --> [Response]
    |-- DELETE /delete?index={index} --> [Read db.json] --> [Delete Submission] --> [Write to db.json] --> [Response]

```

# Conclusion
This backend server works seamlessly with the frontend application to provide a complete form submission system. It handles all the necessary CRUD operations and interacts with the db.json file to store and retrieve submissions.

Feel free to contribute to this project by opening issues or submitting pull requests. Your contributions are greatly appreciated!


## License

[Vedanshi](https://github.com/vedanshi0512)
