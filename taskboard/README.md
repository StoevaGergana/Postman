# About TaskBoard API TestSuite

## Project Overview
TaskBoard is a project management application that allows users to create, update, move, and manage tasks across boards.  
This API TestSuite covers **functional, negative, and security testing**, demonstrating a complete QA workflow.

**Deployed Application:**  
[TaskBoard on Repl.it](https://replit.com/@StoevaGergana/TaskBoardV01#index.js)

---

## 🔧 Tools Used
- Postman (API testing)
- Jira (bug tracking)
- TestRail (test case management)
- GitHub (documentation)

---

## 🧪 Test Coverage

### Functional Tests

#### Positive Tests
| Request | Description | Expected Result |
|---------|-------------|----------------|
| GET | Verify API base route returns available endpoints | 200 OK |
| GET | Verify GET /api/boards returns all boards | 200 OK |
| GET | Verify GET /api/tasks returns all tasks | 200 OK |
| GET | Verify GET /api/tasks/:id returns correct task | 200 OK |
| POST | Create Task with valid data | 201 Created |
| PATCH | Update Task with valid data | 200 OK |
| DELETE | Delete existing task | 200 OK |

---

#### Negative Tests
| Request | Description | Expected Result |
|---------|-------------|----------------|
| POST | Create Task without title | 400 Bad Request |
| GET | Non-existing task ID | 404 Not Found |
| PATCH | Update task with invalid ID | 404 Not Found |
| DELETE | Delete non-existing task | 404 Not Found |

---

### Security Tests
| Test | Description |
|------|------------|
| SQL Injection | Validate API handles malicious input safely |
| Script Injection | Prevent execution of injected scripts |
| Invalid Input | Ensure proper validation and error handling |

---

## 🧾 Test Cases & Execution

Test cases were designed and executed using TestRail and Excel.

📄 [Test Cases](test-cases/taskboard-test-cases.xlsx)  
📄 [Test Run Results](test-cases/taskboard-test-run.xlsx)

The test run includes execution results (Pass/Fail) for functional and negative scenarios.

---

## 🐞 Bug Tracking (Jira)

Bug reports were documented and tracked in Jira.

<img src="screenshots/jira/jira-bugs.png" width="700">

---

## 📊 Test Management (TestRail)

Test cases and execution results were organized in TestRail.

<img src="screenshots/testrail/testrail-testcases.png" width="700">

---

## 📸 API Testing (Postman)

### ✅ Create Task - Success (201 Created)
This test verifies successful task creation with valid data.

<img src="screenshots/postman/create-task-success.png" width="600">

---

### ❌ Create Task - Missing Title (400 Bad Request)
This test verifies validation of required fields.

<img src="screenshots/postman/create-task-fail.png" width="600">

---

### 🔐 SQL Injection Test
This test verifies protection against malicious input.

<img src="screenshots/postman/sql-injection.png" width="600">

---

## ▶️ How to Run
1. Import the collection into Postman  
2. Set environment variables  
3. Run requests individually or via Collection Runner  
4. Validate responses and assertions  

---

## 💡 Key Highlights
- End-to-end QA workflow (API + Test Cases + Bug Tracking)  
- Functional, negative, and security testing  
- Clear and structured documentation  
- Real-world testing approach  
