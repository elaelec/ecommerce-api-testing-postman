# 🛒 E-Commerce API Test Automation Framework

An end-to-end automated API testing suite built with **Postman** and executed via **Newman CLI**. This repository demonstrates core Quality Assurance (QA) engineering practices, including positive/negative test coverage, data-driven testing, dynamic scripting, JSON schema validation, and automated HTML reporting.

---

## 🚀 Key Features & Testing Coverage

* **Full CRUD Operations:** Automated test coverage for `GET`, `POST`, `PUT`, `PATCH`, and `DELETE` endpoints.
* **Positive & Negative Scenarios:** Validating both expected `2xx` success flows and `4xx` error handling (e.g., missing credentials, unauthorized access, non-existent resources).
* **Data-Driven Testing (DDT):** Parameterized test execution using external CSV datasets (`login_data.csv`) to validate multiple user scenarios in a single run.
* **Dynamic Pre-Request Scripting:** Automated generation of unique runtime variables (e.g., `{{random_order_id}}`) using JavaScript before request execution.
* **JSON Schema Validation:** Strict contract testing to ensure response payloads match expected data types and required fields.
* **Environment Management:** Decoupled configuration (`env.json`) for seamless switching across testing environments and shared runtime variables.
* **Automated HTML Reporting:** Detailed execution dashboards generated via `newman-reporter-htmlextra` (`report.html`).

---

## 📊 Latest Test Execution Summary

| Metric | Total | Failed | Status |
| :--- | :---: | :---: | :---: |
| **Total Requests** | 45 | 0 | ✅ Passed |
| **Pre-request Scripts** | 6 | 0 | ✅ Passed |
| **Test Scripts** | 45 | 0 | ✅ Passed |
| **Assertions** | 57 | 0 | ✅ Passed |

---

## 📂 Repository Structure

```text
├── collection.json      # Postman Collection (v2.1) with Positive & Negative test suites
├── env.json             # Environment variables and runtime configurations
├── login_data.csv       # External dataset for Data-Driven login tests
├── report.html          # Generated Newman HTML Extra execution report
└── README.md            # Project documentation
```

## 🛠️ How to Run Locally

### Prerequisites
* [Node.js](https://nodejs.org/) installed on your machine
* Newman & HTML Extra Reporter installed globally:
  ```bash
  npm install -g newman newman-reporter-htmlextra
  ```

### Execution Command
Clone the repository, navigate to the project directory, and run:
```bash
newman run collection.json -e env.json -d login_data.csv -r htmlextra --reporter-htmlextra-export report.html
```

---

## 👩‍💻 Author
**Ela Nezhad** — Electrical Engineer & Junior QA Engineer
