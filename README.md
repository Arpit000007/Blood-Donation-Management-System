**Project Overview**

The Blood Donation Management Service is a comprehensive system designed to streamline the management of blood donations, donor-patient matching, appointment scheduling, and blood inventory tracking. This project was developed by Team_28 to address the challenges of managing blood donations efficiently, ensuring both donors and patients receive timely notifications and updates.

**Functionalities**

1) Donor Registration and Management
Users can register as blood donors, manage their profiles, and view their donation history.

2) Appointment Scheduling
Donors can schedule, reschedule, or cancel blood donation appointments.

3) Blood Inventory Tracking
Real-time tracking and updates of blood inventory levels based on type and quantity.

4) Donor-Patient Matching
The system matches donors with patients based on compatibility criteria using complex algorithms.

5) Notifications and Alerts
Automated notifications for donors and patients regarding appointments, blood needs, and other relevant updates.

**Architectural Design**

The system is based on a microservices architecture, ensuring scalability, flexibility, and ease of maintenance. We also explored the blackboard architecture for certain services and compared both approaches in terms of response time and performance.

**Key Subsystems**

1) User Management Subsystem
Manages user registration, authentication, and profile management.

2) Appointment Management Subsystem
Handles booking, rescheduling, and cancellation of donation appointments.

3) Inventory Management Subsystem
Tracks and manages blood stock levels, ensuring real-time updates.

4) Notification Subsystem
Sends automated alerts and reminders to users regarding appointments and blood donation camps.

5) Health Check Service
Evaluates the health eligibility of potential donors by integrating with health databases.

**Technical Stack**

1) Backend: Microservices architecture with each service having its own database.
2) Authentication: Secure token-based authentication (JWT).
3) Frontend: HTML/CSS, JavaScript.
4) Database: Separate databases per microservice to ensure independence and fault tolerance.

**Performance Analysis**

We implemented the system using two architectural patterns: microservices and blackboard. The response times for different services were compared:

## Performance Comparison: Microservices vs Blackboard

| **Service**            | **Microservice Response Time** | **Blackboard Response Time** |
|------------------------|-------------------------------|------------------------------|
| Donor Registration      | 219.76 ms                     | 264.91 ms                    |
| Login                  | 227.25 ms                     | 364 ms                       |
| Slot Booking           | 555.47 ms                     | 467.72 ms                    |
| Camp Registration      | 435.34 ms                     | 377.17 ms                    |
| Notification           | 216.57 ms                     | 372.53 ms                    |

**Trade-offs Between Architectures**

Microservices Architecture

Pros: Modularity, scalability, independent deployment.

Cons: Higher complexity, challenges in ensuring data consistency.

Blackboard Architecture

Pros: Simplified data management, centralized knowledge.

Cons: Risk of bottlenecks, limited scalability.

**How to Run**

1) Clone the repository:git clone https://github.com/your-username/blood-donation-management.git
2) Install dependencies for each microservice.
3) Set up your environment variables for database configurations and JWT authentication.
4) Run each microservice individually.
5) Access the frontend to register as a donor, schedule appointments, and track inventory.
