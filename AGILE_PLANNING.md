# Agile Planning Document – Health Habit Tracker

---

## 1. Introduction

This document applies Agile methodology to the FitPlan system by translating system requirements and use cases into user stories, organizing them into a prioritized backlog, and planning an initial sprint.

This work builds on:

* Functional Requirements (Assignment 4)
* Use Cases (Assignment 5)

---

## 2. User Stories

| Story ID | User Story                                                                | Acceptance Criteria                       | Priority |
| -------- | ------------------------------------------------------------------------- | ----------------------------------------- | -------- |
| US001    | As a user, I want to register so that I can access the system             | Valid email; password rules; ≤2s response | High     |
| US002    | As a user, I want to log in so that I can access my account securely      | JWT token; HTTP 401 for invalid login     | High     |
| US003    | As a user, I want to create workout plans so that I can organize workouts | Plan saved with exercises, sets, reps     | High     |
| US004    | As a user, I want to log workouts so that I can track activity            | Workout saved with timestamp              | High     |
| US005    | As a user, I want to log meals so that I can track calories               | API fetch ≤2s; fallback available         | High     |
| US006    | As a user, I want calorie tracking so that I can monitor intake           | Updates dynamically; ±5% accuracy         | High     |
| US007    | As a user, I want to view progress so that I can track improvement        | Charts load ≤2s                           | Medium   |
| US008    | As a user, I want to set goals so that I can stay motivated               | Goals saved and tracked                   | Medium   |
| US009    | As a user, I want notifications so that I don’t miss activities           | Sent within ±1 minute                     | Medium   |
| US010    | As an admin, I want secure authentication so that user data is protected  | Password hashing; token expiry            | High     |

---

## 3. Traceability to Requirements

| Story ID | Functional Requirement  | Use Case |
| -------- | ----------------------- | -------- |
| US001    | FR1 – Registration      | UC1      |
| US002    | FR2 – Login             | UC2      |
| US003    | FR3 – Workout Plan      | UC3      |
| US004    | FR4 – Log Workout       | UC4      |
| US005    | FR5 – Log Meal          | UC5      |
| US006    | FR6 – Calorie Tracking  | UC5      |
| US007    | FR7 – Progress Tracking | UC6      |
| US008    | FR8 – Goal Setting      | UC7      |
| US009    | FR9 – Notifications     | UC8      |
| US010    | FR2 – Authentication    | UC2      |

---

## 4. Product Backlog

| Story ID | User Story       | Priority (MoSCoW) | Story Points | Dependencies |
| -------- | ---------------- | ----------------- | ------------ | ------------ |
| US001    | Register         | Must-have         | 3            | None         |
| US002    | Login            | Must-have         | 3            | US001        |
| US003    | Create workout   | Must-have         | 5            | US002        |
| US004    | Log workout      | Must-have         | 3            | US003        |
| US005    | Log meals        | Must-have         | 5            | US002        |
| US006    | Calorie tracking | Must-have         | 3            | US005        |
| US010    | Secure auth      | Must-have         | 5            | US002        |
| US007    | View progress    | Should-have       | 5            | US004, US005 |
| US008    | Goal setting     | Should-have       | 3            | US007        |
| US009    | Notifications    | Could-have        | 3            | US002        |

---

## 5. Sprint Planning

### Sprint Duration

2 Weeks

---

### Sprint Goal

Deliver a Minimum Viable Product (MVP) that allows users to:

* Register and log in
* Create workouts
* Log meals
* Track calories

---

### Selected User Stories

* US001 – Register
* US002 – Login
* US003 – Create workout
* US005 – Log meals
* US006 – Calorie tracking

---

### Sprint Backlog

| Task ID | Task Description          | Assigned To | Hours | Status |
| ------- | ------------------------- | ----------- | ----- | ------ |
| T001    | Database schema design    | Dev         | 6     | To Do  |
| T002    | Registration API          | Dev         | 8     | To Do  |
| T003    | Login API                 | Dev         | 8     | To Do  |
| T004    | Workout API               | Dev         | 10    | To Do  |
| T005    | Meal logging API          | Dev         | 10    | To Do  |
| T006    | Nutrition API integration | Dev         | 8     | To Do  |
| T007    | Calorie logic             | Dev         | 6     | To Do  |
| T008    | Frontend forms            | Dev         | 8     | To Do  |

---

## 6. Reflection

One of the main challenges in this assignment was prioritizing features while working alone. Acting as both the developer and product owner created internal conflict when deciding which features to include in the sprint.

There was a strong temptation to include more advanced features such as notifications and analytics, but Agile principles required focusing on delivering a functional MVP first. This meant prioritizing essential features like authentication, workout tracking, and meal logging.

Another challenge was estimating effort accurately without a team. Assigning story points required careful judgment of complexity and dependencies between tasks.

Additionally, ensuring traceability between requirements, use cases, and user stories required revisiting previous assignments and maintaining consistency.

Overall, this assignment highlighted the importance of incremental delivery, prioritization, and maintaining alignment between system requirements and development planning.
