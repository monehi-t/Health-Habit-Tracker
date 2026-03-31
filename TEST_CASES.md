# Test Cases – Health Habit Tracker

| Test Case ID | Requirement ID | Description    | Steps                        | Expected Result         | Actual Result | Status |
| ------------ | -------------- | -------------- | ---------------------------- | ----------------------- | ------------- | ------ |
| TC001        | FR1            | Register user  | Enter valid email & password | Account created         |               |        |
| TC002        | FR2            | Login user     | Enter valid credentials      | User logged in          |               |        |
| TC003        | FR3            | Create workout | Add workout details          | Workout saved           |               |        |
| TC004        | FR4            | Log workout    | Log completed workout        | Entry stored            |               |        |
| TC005        | FR5            | Log meal       | Enter food item              | Calories calculated     |               |        |
| TC006        | FR6            | Track calories | Add multiple meals           | Total updates correctly |               |        |
| TC007        | FR7            | View progress  | Open dashboard               | Charts displayed        |               |        |
| TC008        | FR9            | Notifications  | Trigger reminder             | Notification sent       |               |        |

---

## Non-Functional Test Scenarios

### Performance Test

* Simulate 1,000 concurrent users logging meals
* Expected: Response time ≤ 2 seconds

---

### Security Test

* Attempt SQL injection on login
* Expected: Input rejected and system remains secure

