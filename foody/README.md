# Foody API Tests

## Project Overview
Foody is a food management web application that allows users to create, search, update, and delete food items.  
This API test collection validates core functionalities including authentication, food management, and search features.

**Deployed Application:**  
[Open Foody App](http://softuni-qa-loadbalancer-2137572849.eu-north-1.elb.amazonaws.com:85)

---

## Test Coverage

### Functional Tests

#### Information Endpoint
| Method | Endpoint | Description | Expected Result |
|--------|----------|-------------|----------------|
| GET | /api/Info/Methods | Retrieve supported API endpoints | 200 OK |

---

#### User Management
| Method | Endpoint | Description | Expected Result |
|--------|----------|-------------|----------------|
| POST | /api/User/Create | Create new user with valid data | 200 OK |
| POST | /api/User/Authentication | Generate access token | 200 OK |

---

#### Food Management (CRUD)
| Method | Endpoint | Description | Expected Result |
|--------|----------|-------------|----------------|
| GET | /api/Food/All | Retrieve all food items | 200 OK |
| POST | /api/Food/Create | Create new food item | 201 Created |
| PATCH | /api/Food/Edit/:foodId | Update existing food item | 200 OK |
| DELETE | /api/Food/Delete/:foodId | Delete food item | 200 OK |

---

#### Search Functionality
| Method | Endpoint | Description | Expected Result |
|--------|----------|-------------|----------------|
| GET | /api/Food/Search?keyword={foodName} | Search food by keyword | 200 OK |

---

## Authentication

All endpoints require Bearer Token authentication.

The token is generated via:
POST /api/User/Authentication

Example:
Authorization: Bearer ```accessToken```


The access token is stored as an environment variable in Postman and reused across requests.

---

## Environment Variables

| Variable | Description |
|----------|------------|
| baseURL | Base API URL |
| accessToken | Bearer authentication token |

Example: 
baseURL = http://softuni-qa-loadbalancer-2137572849.eu-north-1.elb.amazonaws.com:85


---

## How to Run
1. Import the collection into Postman
2. Set the `baseURL` environment variable
3. Authenticate to generate access token
4. Run requests individually or using Collection Runner
5. Validate responses and status codes

---

## Screenshots

### ✅ Get All Foods (200 OK)
This test verifies that the API returns a list of all food items.

<img src="screenshots/get-all-foods.png" width="600">

---

### ✅ Create Food (201 Created)
This test verifies that a new food item is successfully created.

<img src="screenshots/create-food.png" width="600">

---

### ✅ Food Search (200 OK)
This test verifies that the API returns matching food results based on keyword search.

<img src="screenshots/food-search.png" width="600">

---

### ✅ Edit Food (200 OK)
This test verifies that an existing food item can be successfully updated.

<img src="screenshots/edit-food.png" width="600">

---

### ✅ Delete Food (200 OK)
This test verifies that a food item can be successfully deleted.

<img src="screenshots/delete-food.png" width="600">



## Notes
- Covers full CRUD operations for food management  
- Includes authentication and search functionality  
- Uses environment variables for flexible configuration  
- Demonstrates API validation and expected responses
  
