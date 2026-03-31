# System Requirements Document (SRD) – Health Habit-Tracker

---

## 1. Functional Requirements

### FR1: User Registration

The system will allow users to register using a unique email and password.

**Acceptance Criteria:**

* Email must be validated using regex format validation
* Password must be at least 8 characters, including 1 uppercase letter, 1 number, and 1 special character
* Duplicate email registrations will be rejected with an error message
* Registration request will complete within ≤ 2 seconds

---

### FR2: User Login

The system will authenticate users using secure credentials, befor granting access.

**Acceptance Criteria:**

* Invalid login attempts will return HTTP 401 status
* Authentication response time will be ≤ 2 seconds
* Account will lock after 5 consecutive failed attempts

---

### FR3: Create Workout Plan

The system will allow users to create, update, and delete workout plans.

**Acceptance Criteria:**

* Users will be able to define exercises, sets, reps, and duration
* Data will persist in the database immediately after saving
* API will return HTTP 201 on successful creation
* Workout plan creation will complete within ≤ 2 seconds

---

### FR4: Log Workout Activity

The system will allow users to log completed workouts.

**Acceptance Criteria:**

* Logged workouts must include date, duration, and exercises completed
* Data will be stored with timestamp accuracy (ISO 8601 format)
* System will confirm successful logging via HTTP 200 response

---

### FR5: Log Meals

The system will allow users to record meals and nutritional intake.

**Acceptance Criteria:**

* Users will input food name, quantity, and meal type (breakfast/lunch/dinner)
* System will fetch nutritional data via external API within ≤ 2 seconds
* If API fails, the system will allow manual calorie input
* All meal entries must be stored persistently

---

### FR6: Calorie Tracking

The system will calculate total daily calorie intake.

**Acceptance Criteria:**

* Calorie totals will update dynamically after each meal entry
* Daily totals must be accurate within ±5% margin
* The system will display total calories in real-time on dashboard

---

### FR7: Progress Tracking

The system will provide analytics on user progress over time.

**Acceptance Criteria:**

* Charts will display weight, calorie intake, and workout frequency
* Data shall refresh within ≤ 2 seconds of new entry
* Users can filter data by daily, weekly, and monthly views

---

### FR8: Goal Setting

The system will allow users to define and track their fitness goals.

**Acceptance Criteria:**

* Users will set goals (e.g., weight loss, muscle gain)
* The system will calculate progress percentage towards the goal
* Progress will update automatically after new data input

---

### FR9: Notifications

The system will send reminders for workouts and meals.

**Acceptance Criteria:**

* Notifications will be triggered based on user-defined schedules
* The system will send notifications within ±1 minute of the scheduled time
* Failed notifications will be retried up to 3 times

---

### FR10: Dashboard View

The system wiwll provide a centralized dashboard summarizing user activity.

**Acceptance Criteria:**

* Dashboard will load within ≤ 2 seconds
* Display must include:

  * Daily calories
  * Upcoming workouts
  * Progress summary
* Data must reflect latest user activity

---

### FR11: External Nutrition API Integration

The system will integrate with a third-party nutrition API.

**Acceptance Criteria:**

* API response time will be ≤ 2 seconds
* System shall handle API failures gracefully (fallback mechanism)
* API requests will not exceed rate limits (e.g., ≤1000 requests/day)

---

## 2. Non-Functional Requirements

### Usability

* The system will allow users to complete core actions (log meal, log workout) in ≤ 3 clicks
* The interface will achieve a System Usability Scale (SUS) score ≥ 75
* The UI will be responsive across devices (mobile, tablet, desktop)

---

### Deployability

* The system will be deployable using containerization (e.g., Docker)
* The system will support CI/CD pipelines for automated deployment
* The system will support deployment on Linux-based servers

---

### Maintainability

* The system will follow a modular architecture (separation of concerns)
* Codebase will maintain ≥70% unit test coverage
* API documentation will be provided
* Code will follow consistent linting and formatting standards

---

### Scalability

* The system will support ≥1,000 concurrent users
* The architecture will support horizontal scaling
* The database will support indexing for optimized query performance

---

### Security

* All user data will be encrypted in transit using industry standards.
* Passwords will be hashed using bcrypt with salt
* Role-based access control (RBAC) will be enforced

---

### Performance

* API requests will respond within ≤ 2 seconds
* The system shall handle 95% of requests without delay
* Database queries will execute within ≤ 500ms
* Frontend page load time shall be ≤ 3 seconds

---

### Reliability

* The system will maintain ≥99% uptime
* Backup mechanisms will be implemented
* System will recover from failure within ≤ 5 minutes

---

### Compatibility

* The system will support latest versions of Chrome, Firefox, and Edge
* The system will function across Windows, macOS, and Linux platforms
* APIs will follow REST standards for interoperability


