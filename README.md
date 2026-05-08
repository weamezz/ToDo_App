Overview

This project validates the core functionality of a RESTful TODO API. It ensures that the system correctly handles user registration, secure authentication via Bearer Tokens, and full CRUD (Create, Read, Update, Delete) operations on tasks.
Tech Stack

* **Tool:** Postman
* **Scripting:** JavaScript (Postman Sandbox)
* **API Architecture:** REST
* **Authentication:** Dynamic Bearer Token

 Key Features & Test Scenarios

### 1. User Authentication Flow
* **Automatic Registration:** Uses Postman dynamic variables (`{{$randomFirstName}}`, `{{$randomEmail}}`) to create unique users for every test run.
* **Token Management:** Automatically extracts the `access_token` from the registration response and saves it to the environment for subsequent authorized requests.

### 2. Task Lifecycle (CRUD)
* **Create (POST):** Adds a new task and captures the generated `taskID`.
* **Update (PUT):** Modifies the task status (e.g., marking as completed) using the stored `taskID`.
* **Delete (DELETE):** Removes the task from the system to ensure environment cleanup.

### 3. Advanced Scripting
* **Pre-request Scripts:** Dynamic data generation before requests are sent.
* **Tests Scripts:**
    * Status code validation (201 Created, 200 OK).
    * Response body functional assertions.
    * Dynamic environment variable updates for seamless request chaining.

## 📁 Project Structure

* `TODO.postman_collection.json`: The main collection file containing all requests and test scripts.
* `Environment Configuration`: (Ensure to set your `base_url` variable).
