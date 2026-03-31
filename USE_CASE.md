# Use Case Specifications – Health Habit Tracker

---

## UC1: Register User

**Actor:** Fitness User
**Description:** User creates a new account

**Preconditions:**

* User is not registered

**Postconditions:**

* Account is created and stored in database

**Basic Flow:**

1. User enters email and password
2. System validates input
3. System creates account
4. Confirmation is displayed

**Alternative Flow:**

* Invalid email → error message
* Duplicate email → registration rejected

---

## UC2: Login User

**Actor:** Fitness User

**Preconditions:**

* User account exists

**Postconditions:**

* User is authenticated and receives token

**Basic Flow:**

1. User enters credentials
2. System validates credentials
3. System grants access

**Alternative Flow:**

* Incorrect credentials → access denied

---

## UC3: Create Workout Plan

**Actor:** Fitness User

**Preconditions:**

* User is logged in

**Postconditions:**

* Workout plan is saved

**Basic Flow:**

1. User enters workout details
2. System validates data
3. System stores plan

---

## UC4: Log Workout

**Actor:** Fitness User

**Preconditions:**

* User is logged in

**Postconditions:**

* Workout log is saved

**Basic Flow:**

1. User selects workout
2. User logs completion
3. System stores data

---

## UC5: Log Meal

**Actor:** Fitness User

**Preconditions:**

* User is logged in

**Postconditions:**

* Meal is recorded with calories

**Basic Flow:**

1. User enters food item
2. System queries Nutrition API
3. System calculates calories
4. Data is saved

**Alternative Flow:**

* API failure → manual input required

---

## UC6: Track Progress

**Actor:** Fitness User

**Preconditions:**

* User has logged data

**Postconditions:**

* Progress data is displayed

**Basic Flow:**

1. User opens dashboard
2. System retrieves data
3. Charts are displayed

---

## UC7: Set Goals

**Actor:** Fitness User

**Preconditions:**

* User is logged in

**Postconditions:**

* Goal is saved and tracked

**Basic Flow:**

1. User sets goal
2. System stores goal
3. Progress tracking begins

---

## UC8: Send Notifications

**Actor:** System

**Preconditions:**

* Notification schedule exists

**Postconditions:**

* Notification is sent

**Basic Flow:**

1. Scheduler triggers event
2. System sends notification via email

**Alternative Flow:**

* Email failure → retry mechanism

