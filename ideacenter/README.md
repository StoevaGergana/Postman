# IdeaCenter API Tests

## Project Overview
IdeaCenter is a web application that allows users to create, manage, and share ideas.  
This API test collection covers core functionalities such as user authentication, idea management, and system behavior validation.

---
**Deployed Application:**  
http://softuni-qa-loadbalancer-2137572849.eu-north-1.elb.amazonaws.com:83

## Test Coverage

### Functional Tests

#### Information & System Endpoints
| Method | Endpoint | Description | Expected Result |
|--------|----------|-------------|----------------|
| GET | /api/Info/Methods | Retrieve supported API endpoints | 200 OK |

---

#### User Management
| Method | Endpoint | Description | Expected Result |
|--------|----------|-------------|----------------|
| POST | /api/User/Create | Create new user with valid data | 200 OK |
| POST | /api/User/Authentication | Authenticate user and retrieve token | 200 OK |

---

#### Idea Management
| Method | Endpoint | Description | Expected Result |
|--------|----------|-------------|----------------|
| GET | /api/Idea/All | Retrieve all ideas | 200 OK |
| POST | /api/Idea/Create | Create new idea with valid data | 200 OK |
| PUT | /api/Idea/Edit | Edit existing idea | 200 OK |
| PUT | /api/Idea/Edit | Edit idea with different data set | 200 OK |
| DELETE | /api/Idea/Delete | Delete idea by ID | 200 OK |

---

## Authentication

All endpoints require Bearer Token authentication.

The token is generated via:
POST /api/User/Authentication

Example: 
Authorization: Bearer accessToken


---

## How to Run
1. Import the collection into Postman
2. Set up environment variables (token if needed)
3. Execute requests individually or run the full collection
4. Validate responses and status codes

---

## Screenshots

### ✅ Get All Ideas (200 OK)
This test verifies that the API successfully returns a list of all ideas.

<img src="ideacenter/screenshots/get-all-ideas.png" width="600">

---

### ✅ Create User (200 OK)
This test verifies that a new user can be successfully registered with valid data.

<img src="screenshots/ideacenter/create-user.png" width="600">

---

### ✅ Authentication Token (200 OK)
This test verifies that the API returns a valid authentication token when correct credentials are provided.

<img src="screenshots/ideacenter/authentication-token.png" width="600">

---

### ✅ Create Idea (200 OK)
This test verifies that a new idea can be successfully created with valid input data.

<img src="screenshots/ideacenter/create-idea.png" width="600">

---

### ✅ Edit Idea (200 OK)
This test verifies that an existing idea can be successfully updated.

<img src="screenshots/ideacenter/edit-idea.png" width="600">

---

### ✅ Delete Idea (200 OK)
This test verifies that an idea can be successfully deleted by ID.

<img src="screenshots/ideacenter/delete-idea.png" width="600">

---

## Notes
- All tests validate response status codes and basic functionality  
- Authentication is required for most endpoints  
- The collection demonstrates CRUD operations for ideas  
- Covers core API flows: **Create → Read → Update → Delete**


