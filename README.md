# airbnb-clone-project
The backend for the Airbnb Clone project provides a robust and scalable foundation for managing user interactions, property listings, bookings, and payments. This backend will support various functionalities required to mimic the core features of Airbnb, ensuring a smooth experience for users and hosts.

### **Team Roles**
1. **Backend Developer**: Responsible for implementing API endpoints, database schemas, and business logic.
2. **Database Administrator**: Manages database design, indexing, and optimizations.
3. **DevOps Engineer**: Handles deployment, monitoring, and scaling of the backend services.
4. **QA Engineer**: Ensures the backend functionalities are thoroughly tested and meet quality standards.

### **Technology Stack**
* **Django:** A high-level Python web framework used for building the RESTful API.
* **Django REST Framework:** Provides tools for creating and managing RESTful APIs.
* **PostgreSQL:** A powerful relational database used for data storage.
* **GraphQL:** Allows for flexible and efficient querying of data.
* **Celery:** For handling asynchronous tasks such as sending notifications or processing payments.
* **Redis:** Used for caching and session management.
* **Docker:** Containerization tool for consistent development and deployment environments.
* **CI/CD Pipelines:** Automated pipelines for testing and deploying code changes.

### **Database Design**
**Users** Fields: id, name and surename, email Relationships: User can see many properties
**Properties** Fields: id, PropertyName, Propertyaddress Relationships: A single property can have only one booiking
**Bookings** Fields: id, CheckInDate, CheckoutDate Relationships: One booking for one user
**Reviews** Field: id, Rating, date&time Relationships: Reviews for many users
**Payments** Field: id, dateOfPayment, Relationships: bill/amount 