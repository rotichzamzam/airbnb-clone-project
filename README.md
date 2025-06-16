# Airbnb Clone Project

## Overview
The Airbnb Clone Project is a full-stack web application that simulates a real-world booking platform like Airbnb. It focuses on backend architecture, API development, secure database design, and CI/CD deployment practices.

## Project Goals
- Build a scalable backend with Django and MySQL
- Secure user data and transactions
- Collaborate effectively using GitHub workflows
- Automate testing and deployment using CI/CD

## Tech Stack
- Django
- MySQL
- GraphQL
- Docker
- GitHub Actions

## Team Roles

- **Backend Developer**: Implements the logic and endpoints of the application using Django and GraphQL.
- **Database Administrator (DBA)**: Designs, optimizes, and secures the MySQL database.
- **DevOps Engineer**: Sets up Docker containers and CI/CD pipelines using GitHub Actions.
- **Security Engineer**: Ensures user data and APIs are secured with authentication, authorization, and rate limiting.
- **Technical Writer**: Documents project workflows, APIs, and system architecture.

## Technology Stack

- **Django**: Web framework for handling business logic and building APIs.
- **MySQL**: Relational database to manage structured data like users, bookings, and reviews.
- **GraphQL**: API query language for efficient client-server communication.
- **Docker**: Containerization platform to ensure consistent environments during development and deployment.
- **GitHub Actions**: CI/CD tool for automating tests, builds, and deployments.


## Database Design

### Entities and Key Fields:

- **User**
  - id
  - name
  - email
  - password
  - role (host or guest)

- **Property**
  - id
  - title
  - description
  - price
  - owner_id (FK to User)

- **Booking**
  - id
  - user_id (FK to User)
  - property_id (FK to Property)
  - start_date
  - end_date

- **Review**
  - id
  - user_id (FK to User)
  - property_id (FK to Property)
  - rating
  - comment

- **Payment**
  - id
  - booking_id (FK to Booking)
  - amount
  - status

### Relationships:
- A user can own multiple properties.
- A booking links one user to one property.
- A user can review many properties.
- Each booking has one payment.

## Feature Breakdown

- **User Management**  
  Handles user registration, login, role assignment and profile updates.

- **Property Management**  
  Allows hosts to add, update and delete listings with images and descriptions.

- **Booking System**  
  Enables users to check availability and book properties securely.

- **Review System**  
  Lets users leave feedback and ratings for properties they have stayed in.

- **Payment Integration**  
  Manages secure payments and links them to bookings with real-time status updates.

## API Security

### Security Measures:
- **Authentication**: Use token-based authentication (JWT) to verify user identity.
- **Authorization**: Role-based access control to restrict endpoints.
- **Rate Limiting**: Prevent abuse by limiting requests per user/IP.

### Importance:
- **Authentication** ensures only verified users can access resources.
- **Authorization** prevents users from performing actions beyond their role.
- **Rate Limiting** protects the system from DDoS or brute-force attacks.
- **Secure Payments** protect user financial data and prevent fraud.

## CI/CD Pipeline

### What It Is:
CI/CD (Continuous Integration/Continuous Deployment) automates testing, building, and deployment processes to improve reliability and speed.

### Tools:
- **GitHub Actions**: Automate testing and deployments on code changes.
- **Docker**: Containerize the app to ensure consistency across environments.

### Why It Matters:
- Reduces human error
- Speeds up delivery
- Ensures tested, production-ready code is deployed every time
