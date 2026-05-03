# Health Habit-Tracker Reflection 
---
## Requirements Engineering

### Challenges Faced

One of the main challenges in this assignment was trying to balance the different needs of stakeholders. For example, fitness users require a simple and intuitive interface, while developers prioritize system structure and maintainability.

Another challenge was making sure that functional requirements remained realistic and achievable within the scope of an individual project. There was a need to avoid overcomplicating the system while still addressing all stakeholder concerns.

Additionally, conflicts where identified between performance and feature richness. For example, real-time notifications improve user engagement but may impact the system performance and scalability.

### Lessons Learned

This assignment highlighted the importance of clearly defining requirements early in the development process. It also showed how different stakeholders have competing priorities that must be balanced carefully.

---

## Use Case & Testing

One of the main challenges in this portions of the assignment was translating functional requirements into detailed use cases. While requirements describe what the system should do, use cases required a deeper understanding of how users interact with the system step by step.

Another challenge was ensuring consistency between assignments. All use cases had to align with previously defined functional requirements, which required careful tracing and refinement.

Developing test cases also introduced complexity, especially in ensuring coverage of both normal and edge scenarios. It was important to define clear expected results so that system behavior could be validated effectively.

Additionally, balancing simplicity and completeness was difficult. Including too much detail made the use cases complex, while too little detail reduced clarity.

Overall, this process improved understanding of system behavior, user interaction, and the importance of validation through testing. It also reinforced how different stages of software engineering are interconnected.

---

## Agile Planning

One of the main challenges in this assignment was prioritizing features while working alone. Acting as both the developer and product owner created internal conflict when deciding which features to include in the sprint.

There was a strong temptation to include more advanced features such as notifications and analytics, but Agile principles required focusing on delivering a functional MVP first. This meant prioritizing essential features like authentication, workout tracking, and meal logging.

Another challenge was estimating effort accurately without a team. Assigning story points required careful judgment of complexity and dependencies between tasks.

Additionally, ensuring traceability between requirements, use cases, and user stories required revisiting previous assignments and maintaining consistency.

Overall, this assignment highlighted the importance of incremental delivery, prioritization, and maintaining alignment between system requirements and development planning.

---

## Domain Modeling & Class Diagram

Designing the domain model and class diagram for the Health Habit Tracker system was one of the most challenging but insightful parts of the project. One of the main difficulties was identifying the correct level of abstraction for entities. Initially, there was a tendency to either overcomplicate the model by introducing too many entities or oversimplify it by merging concepts that should remain separate.

Another challenge was defining relationships accurately. Deciding when to use composition versus association required careful thought. For example, the relationship between WorkoutPlan and Exercise was modeled as composition because exercises cannot exist independently of a workout plan. However, relationships such as User and Meal were modeled as associations since meals can exist independently but are linked to a specific user.

Aligning the class diagram with previous assignments also required revisiting earlier work. Functional requirements, use cases, and user stories had to be consistent with the domain model. This highlighted the importance of traceability in software engineering. For example, the Meal entity directly supports the "Log Meal" use case and the corresponding functional requirement, ensuring continuity across assignments.

Another challenge was defining appropriate methods for each class. It was important to avoid including too much business logic in a single class, which would violate object-oriented design principles. Instead, responsibilities were distributed across classes to maintain modularity and separation of concerns.

Trade-offs were also necessary. While inheritance could have been used for different types of users (e.g., Beginner User, Coach), it was simplified into a single User class with roles to avoid unnecessary complexity. This decision improves maintainability but reduces specialization.

One key lesson learned is the importance of designing systems with future scalability in mind. The modular structure of the class diagram allows for future enhancements, such as integrating wearable devices or adding advanced analytics.

Overall, this assignment improved my understanding of object-oriented design principles, including abstraction, encapsulation, and relationships between classes. It also reinforced the importance of aligning design artifacts with system requirements and user interactions.

---




