# API Testing with Postman & Newman

This project contains a suite of automated API tests for the public REST API at [reqres.in](https://reqres.in). The tests are created in Postman and can be executed manually within Postman or automated via Newman – a CLI-based test runner.

## 🎯 Purpose
To demonstrate proficiency in API testing, error handling, and automation within the QA field. The project simulates real-world user flows such as authentication, data retrieval, resource creation, and deletion.

## 🚀 Features
- ✅ **Login:** Validation for successful and failed (missing password) attempts.
- 👥 **User Management:** Fetching user lists and validating data structure.
- ➕ **Resource Creation:** Adding new users to the system.
- 🗑️ **Resource Deletion:** Verifying the correct removal of users.
- 🔄 **Validations:** Checking HTTP status codes, JSON response bodies, and error messages.

## 🧰 Tools Used
- **Postman:** Test development and documentation.
- **Newman:** Command-line execution for automation.
- **JavaScript:** Scripting for test assertions.
- **reqres.in:** The hosted REST API used for testing.

## 📦 Project Structure
```text
API-Testing-with-Postman-Newman/
├── README.md
├── collections/
│   └── QA-Demo.postman_collection.json
├── environments/
│   └── reqres-environment.postman_environment.json
└── reports/
    └── (generated via Newman CLI)

🛠️ Getting Started

1. Clone the project

bash
git clone [https://github.com/Sobhan-G/API-Testing-with-Postman-Newman.git](https://github.com/Sobhan-G/API-Testing-with-Postman-Newman.git)
cd API-Testing-with-Postman-Newman

2. Install Newman

ash
npm install -g newman


3. Run the test suite

newman run collections/Sobhan-QA-Demo.postman_collection.json \
  -e environments/reqres-environment.postman_environment.json


4. Generate HTML report (optional)
newman run collections/Sobhan-QA-Demo.postman_collection.json \
  -e environments/reqres-environment.postman_environment.json \
  -r cli,html --reporter-html-export reports/test-report.html

Test Name,Endpoint,Description

Login - Success,POST /api/login,"Successful login, verifies token creation."
Login - Fail,POST /api/login,Failed login attempt (missing password).
Get Users,GET /api/users?page=2,Ensures user data is retrieved correctly.
Create User,POST /api/users,Validates new user creation.
Delete User,DELETE /api/users/2,Confirms user deletion.

📈 Results
Example of CLI output:

→ Login - Success
  ✓ Status 200
  ✓ Token is a string

→ Login - Fail
  ✓ Status 400
  ✓ Error message: "Missing password"

📚 Key Learnings
This project has enhanced my practical understanding of:

API design and testing strategies.

Automating tests using Newman.

Error handling and test-driven scenarios.

Preparing for CI/CD integration.

🧩 Future Enhancements
Integrate CI/CD via GitHub Actions.

Implement Data-Driven Testing (using JSON/CSV data files).

Expand the suite to cover other API environments (e.g., Auth, E-commerce).
