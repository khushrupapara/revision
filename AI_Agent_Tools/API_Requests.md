# API Requests

## Quick Overview

| Name        | Definition                                                     | Example              |
| ----------- | -------------------------------------------------------------- | -------------------- |
| API         | A way for one application to communicate with another service. | Weather API          |
| API Request | A message sent to an API to request data or perform an action. | Get today's weather  |
| HTTP Method | Describes what the request wants to do.                        | `GET`, `POST`        |
| Endpoint    | The URL where an API request is sent.                          | `/users`             |
| JSON        | A common format for sending and receiving structured data.     | `{"city": "Rajkot"}` |

## 1. API Request

**Definition:** An API request allows an AI agent to communicate with an external service to get data or perform an action.

**Example:**

```text
User
  ↓
AI Agent
  ↓
API Request
  ↓
Weather API
  ↓
JSON Response
  ↓
AI Agent
  ↓
Answer
```

**Instructions:**

* Use APIs when the agent needs data or functionality from another service.
* An API request usually contains a URL, HTTP method, and sometimes parameters or a request body.
* The API processes the request and sends a response.
* Protect API keys and other authentication credentials.

## 2. HTTP Methods

**Definition:** HTTP methods tell an API what type of operation the client wants to perform.

**Example:**

```http
GET /users
```

```http
POST /users
Content-Type: application/json

{
  "name": "Alice"
}
```

**Instructions:**

* `GET` is commonly used to retrieve data.
* `POST` is commonly used to send data or create a resource.
* `PUT` or `PATCH` is commonly used to update data.
* `DELETE` is commonly used to remove a resource.

## 3. Endpoint

**Definition:** An endpoint is a specific URL where an API accepts requests for a particular resource or operation.

**Example:**

```text
https://api.example.com/users
```

```text
https://api.example.com/weather
```

**Instructions:**

* Use the endpoint specified by the API documentation.
* Different endpoints usually provide different resources or operations.
* Check required parameters before sending the request.
* Do not assume every API uses the same endpoint structure.

## 4. JSON Request and Response

**Definition:** JSON is a common format APIs use to send structured data between applications.

**Example:**

```json
{
  "city": "Rajkot",
  "temperature": 32,
  "condition": "Sunny"
}
```

**Instructions:**

* JSON stores data as key-value pairs and other structured values.
* An API may accept JSON in a request body.
* An API may return JSON in its response.
* Always check the API documentation for the expected JSON structure.

## 5. AI Agent + API

**Definition:** An AI agent can decide when to call an API, create the required request, read the response, and use the result to complete a task.

**Example:**

```text
User: What is the weather in Rajkot?

Agent:
1. Understands the request.
2. Calls the weather API.
3. Receives current weather data.
4. Reads the response.
5. Gives the user an answer.
```

**Instructions:**

* Use APIs to give agents access to current data and external services.
* Validate API responses before using them.
* Handle errors such as timeouts, invalid requests, and authentication failures.
* Use proper authentication and access controls for protected APIs.

## Quick Memory

```text
API → Bridge between applications
Request → Message sent to an API
Method → What the request wants to do
Endpoint → Where the request is sent
JSON → Structured data format
Response → Data returned by the API
```
