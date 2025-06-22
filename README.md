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
 * **Users** 
    + **Fields**: id, name and surename, email 
 * **Properties** 
    + **Fields**: id, PropertyName, Propertyaddress
    + **Fields**: id, CheckInDate, CheckoutDate
 * **Reviews** 
    + **Field**: id, Rating, date&time
 * **Payments** 
    + **Field**: id, dateOfPayment, amountPaid
  **Relationships**:
    1. **User ↔ Properties**
        + A user can create many listings
        + A listing is hosted by one user
    2. **User ↔ Booking**
        + A user can book many listings
        + A booking is made by one user
    3. **Properties ↔ Booking**
        + A listing can be booked many times
        + A booking is for one specific listing
    4. **Booking ↔ Payment**
        + A booking results in one or more payments
        + A payment is tied to one booking
    5. **User ↔ Review**
        + A user can leave many reviews
        + A review is for one listing and written by one user