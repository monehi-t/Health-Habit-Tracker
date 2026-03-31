# Traceability Matrix – Health Habit Tracker

## Overview

This traceability matrix maps **Functional Requirements (FRs)** to corresponding **Use Cases (UCs)** and **Test Cases (TCs)** to ensure full system coverage and validation.

---

## Traceability Matrix

| Requirement ID | Requirement Description   | Use Case ID | Use Case Name       | Test Case ID | Test Description                     |
| -------------- | ------------------------- | ----------- | ------------------- | ------------ | ------------------------------------ |
| FR1            | User Registration         | UC1         | Register User       | TC001        | Register user with valid credentials |
| FR2            | User Login                | UC2         | Login User          | TC002        | Login with valid credentials         |
| FR3            | Create Workout Plan       | UC3         | Create Workout Plan | TC003        | Create and save workout              |
| FR4            | Log Workout               | UC4         | Log Workout         | TC004        | Log completed workout                |
| FR5            | Log Meal                  | UC5         | Log Meal            | TC005        | Log meal and calculate calories      |
| FR6            | Calorie Tracking          | UC5         | Log Meal            | TC006        | Verify calorie total updates         |
| FR7            | Progress Tracking         | UC6         | Track Progress      | TC007        | Display progress charts              |
| FR8            | Goal Setting              | UC7         | Set Goals           | TC007        | Track progress toward goal           |
| FR9            | Notifications             | UC8         | Send Notifications  | TC008        | Trigger notification                 |
| FR10           | Dashboard View            | UC6         | Track Progress      | TC007        | Dashboard loads with updated data    |
| FR11           | Nutrition API Integration | UC5         | Log Meal            | TC005        | Fetch nutritional data               |

---

## Coverage Analysis

### Requirement Coverage

All functional requirements (FR1–FR11) are mapped to at least one use case and one test case, ensuring full system coverage.

---

### Use Case Coverage

Each use case is linked to one or more requirements and validated through corresponding test cases.

---

### Test Coverage

All critical system functionalities are validated through defined test cases. Both **functional and non-functional aspects** are covered.

---

## Non-Functional Traceability

| Non-Functional Requirement | Test Case | Description                     |
| -------------------------- | --------- | ------------------------------- |
| Performance                | NFTC001   | Simulate 1,000 concurrent users |
| Security                   | NFTC002   | Test SQL injection prevention   |

---

## Conclusion

This traceability matrix ensures that all system requirements are:

* Properly implemented through use cases
* Fully validated through test cases
* Clearly linked for maintainability and future updates

This improves system reliability, reduces development gaps, and ensures alignment with stakeholder needs.
