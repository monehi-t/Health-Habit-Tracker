# Use Case Diagram – Health Habit Tracker

## Diagram

```mermaid
graph TD

%% Actors
User[Fitness User]
Beginner[Beginner User]
Coach[Fitness Coach]
Admin[System Admin]
API[Nutrition API]
Email[Email Service]

%% Use Cases
Register((Register Account))
Login((Login))
CreateWorkout((Create Workout Plan))
LogWorkout((Log Workout))
LogMeal((Log Meal))
TrackCalories((Track Calories))
ViewProgress((View Progress))
SetGoals((Set Goals))
ReceiveNotifications((Receive Notifications))
ManageUsers((Manage Users))

%% Relationships
User --> Register
User --> Login
User --> CreateWorkout
User --> LogWorkout
User --> LogMeal
User --> TrackCalories
User --> ViewProgress
User --> SetGoals
User --> ReceiveNotifications

Beginner --> CreateWorkout
Coach --> ViewProgress

Admin --> ManageUsers

LogMeal --> API
ReceiveNotifications --> Email
```

---

## Explanation

### Key Actors

* **Fitness User**: Primary user interacting with all the system features.
* **Beginner User**: Subtype of user needing simplified system interactions.
* **Fitness Coach**: Monitors user progress.
* **System Admin**: Manages system users and operations.
* **Nutrition API**: External system providing nutrition food data.
* **Email Service**: Sends out notifications.

---

### Relationships

* **Include Relationship**:
  Logging the meals is dependent on fetching nutritional data from the Nutrition API.

* **External Interaction**:
  Notifications rely on the Email Service.

* **Actor Specialization**:
  Beginner User is a specialized type of Fitness User.

---

### Stakeholder Alignment

This diagram addresses:

* Users need for **tracking workouts and meals**
* Coaches need for **monitoring progress**
* Admins need for **system control**
* System integration concerns (API + notifications)

