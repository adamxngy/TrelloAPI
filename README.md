# Trello API Automation Project

[![Postman Collection](https://img.shields.io/badge/Postman-Collection-orange?logo=postman)](https://www.postman.com/)
[![Trello API](https://img.shields.io/badge/API-Trello-blue?logo=trello)](https://developer.atlassian.com/cloud/trello/rest/)

---
## About The Project

This project demonstrates how to interact with the Trello API to automate the creation, updating, retrieval, and deletion of various Trello elements like boards, lists, and cards using Postman. The setup leverages Postman environments, automated scripts, and dynamic variables for full-cycle testing and management of Trello entities.

---

## Project Features

- Automated Trello board, list, and card creation with random names.
- Dynamic ID handling using environment variables,no need for manual copy-pasting.
- Postman test scripts to validate API responses, status codes, and performance.
- Complete CRUD (Create, Read, Update, Delete) operations for all Trello entities.
- Utilizes Postman pre-request and test scripts to streamline workflows.

---

## Environment Setup

### Environment Variables Used:
- `base_url`
- `key`
- `token`
- `board_id`
- `list_id`
- `card_id`
- `board_name`
- `list_name`
- `card_name`

---

## Requests Overview

### 1. **Create a Board**
- **Method:** `POST`
- **Automation:** Random name and background color generation.
- **Tests:**
  - `status === 200`
  - Response contains `id`, `name`, and `url`
  - Board name matches `{{board_name}}`
  - Store `board_id` for later use

---

### 2. **Get a Created Board**
- **Method:** `GET`
- **Tests:** `status === 200`

---

### 3. **Create a New List**
- **Method:** `POST`
- **Automation:** Random list name
- **Tests:** `status === 200`
- Store `list_id` for later use

---

### 4. **Get a Created List**
- **Method:** `GET`
- **Tests:** `status === 200`

---

### 5. **Create a New Card**
- **Method:** `POST`
- **Automation:** Random card name
- **Tests:** `status === 200`
- Store `card_id` for later use

---

### 6. **Get a Created Card**
- **Method:** `GET`
- **Tests:** `status === 200`

---

### 7. **Update Board**
- **Method:** `PUT`
- **Params:** `name = new name`
- **Tests:** `status === 200`

---

### 8. **Get Updated Board**
- **Method:** `GET`
- **Tests:** `status === 200`

---

### 9. **Update List**
- **Method:** `PUT`
- **Params:** `name = new name`
- **Tests:** `status === 200`

---

### 10. **Get Updated List**
- **Method:** `GET`
- **Tests:** `status === 200`

---

### 11. **Update Card**
- **Method:** `PUT`
- **Params:** `name = new name`
- **Tests:** `status === 200`

---

### 12. **Get Updated Card**
- **Method:** `GET`
- **Tests:** `status === 200`

---

### 13. **Delete Card**
- **Method:** `DELETE`
- **Tests:** `status === 200`

---

### 14. **Get Deleted Card**
- **Method:** `GET`
- **Expected:** `status === 404`

---

### 15. **Archive List**
- **Method:** `PUT`
- **Params:** `value = true`
- **Tests:** `status === 200`

---

### 16. **Get Archived List**
- **Method:** `GET`
- **Tests:** `status === 200`

---

### 17. **Delete Board**
- **Method:** `DELETE`
- **Tests:** `status === 200`

---

### 18. **Get Deleted Board**
- **Method:** `GET`
- **Expected:** `status === 404`

---

## Additional Automation

- All requests include a test to check response time is under **1600ms**.
- Random names are generated using pre-request scripts and saved as variables.
- Postman variables are used to automatically pass IDs between requests.

---

## Files Included in Repository

- `Trello APIs.postman_collection.json`
- `Trello APIs Environment.postman_environment.json`
- `README.md`

---

## Prerequisites

- A [Trello API key and token](https://trello.com/app-key)
- Postman installed
- Internet access
