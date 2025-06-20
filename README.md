# airbnb-clone-project
Project Overview: Airbnb Clone
The Airbnb Clone Project is a full-stack software development initiative designed to replicate the functionality and architecture of a real-world booking platform like Airbnb. The goal is to equip learners with hands-on experience in building scalable, secure, and collaborative web applications that follow industry best practices.

Through this project, participants will gain practical exposure to backend system architecture, relational database design, secure API development, and CI/CD deployment workflows. Additionally, the project emphasizes teamwork, version control, and documentation, preparing developers for real-world software engineering environments.

## Project Goal
The primary goal of the Airbnb Clone Project is to simulate the end-to-end development of a booking platform, enabling learners to:

Understand and apply modern backend design patterns

Implement secure, production-ready APIs

Collaborate effectively using GitHub

Design scalable databases and deploy applications using CI/CD pipelines

Integrate various technologies into a unified, efficient system

## Technology Stack
Backend Framework: Django (Python)

Database: MySQL

API Layer: GraphQL

Version Control & Collaboration: Git & GitHub

CI/CD: Docker, GitHub Actions (or similar platforms)

Documentation: Markdown

Security: API authentication & authorization best practices

# Team Roles
 ## Team Roles Overview
### 🔍 Business Analyst (BA)
Translates business needs into clear, actionable requirements.

Analyzes customer workflows and bridges the gap between stakeholders and developers.

### 🎯  Product Owner (PO)
Owns the product vision and strategy.

Defines and prioritizes the product backlog to align with business goals and user needs.

### 📅  Project Manager (PM)
Ensures timely and budget-conscious delivery of the product.

Facilitates team coordination, progress tracking, and stakeholder communication.

### 🎨 UI/UX Designer
Designs intuitive and visually appealing user interfaces.

Crafts user journeys through research, wireframes, and prototyping to optimize experience and engagement.

### 🏗️  Software Architect
Defines the system's high-level structure and tech stack.

Sets coding standards, selects tools, and ensures scalability and security.

### 💻 Software Developer
Implements front-end and back-end features.

Solves technical issues, writes code, and builds application logic and integrations.

### ✅  Quality Assurance (QA) Engineer
Verifies that the product meets all functional and non-functional requirements.

Conducts manual and exploratory testing and ensures quality at every stage.

### ⚙️ Test Automation Engineer
Develops and maintains automated test scripts.

Enhances testing efficiency and coverage with a maintainable automation framework.

### 🚀 DevOps Engineer
Bridges development and operations through automation.

Builds and manages CI/CD pipelines for efficient, reliable deployments.

# Technology Stack
## Technology	Purpose
### Django
A high-level Python web framework used for building robust backend systems, handling authentication, routing, and RESTful/GraphQL APIs.

### MySQL
A reliable, relational database system used to store and manage structured application data like users, listings, and bookings.

### GraphQL	
A flexible API query language used to efficiently fetch and manipulate nested and complex data from the backend.

### Docker	
A containerization tool used to package the application and its dependencies for consistent development and deployment environments.

### Git & GitHub
Used for version control, team collaboration, and maintaining the project repository.

### GitHub Actions
A CI/CD automation tool used to build, test, and deploy the application seamlessly on every update.

Markdown	Used to format documentation files like README.md for better readability and structure.

# Database Design
This project models a simplified version of the Airbnb platform. Below are the key entities in the system, along with important fields and how they relate to one another:

### 🔹 Users
Represents guests and hosts using the platform.

Key Fields:

id: Unique identifier

name: Full name of the user

email: Email address (unique)

is_host: Boolean to indicate if the user is a host

date_joined: Account creation timestamp

### Relationships:

A user can own multiple properties

A user can make multiple bookings

A user can write multiple reviews

### 🔹 Properties
Represents listings available for rent.

Key Fields:

id: Unique identifier

owner_id: Foreign key to Users (host)

title: Property name

location: City/address

price_per_night: Cost per night

### Relationships:

A property belongs to one user (host)

A property can have many bookings

A property can have many reviews

### 🔹 Bookings
Represents a reservation made by a user.

Key Fields:

id: Unique identifier

user_id: Foreign key to Users (guest)

property_id: Foreign key to Properties

check_in: Start date

check_out: End date

### Relationships:

A booking belongs to one user

A booking is for one property

A booking can have one payment

### 🔹 Reviews
Represents feedback left by users after a stay.

Key Fields:

id: Unique identifier

user_id: Foreign key to Users

property_id: Foreign key to Properties

rating: Numeric score (e.g., 1–5)

comment: Text content of the review

### Relationships:

A review belongs to one user

A review belongs to one property

### 🔹 Payments
Represents financial transactions for bookings.

Key Fields:

id: Unique identifier

booking_id: Foreign key to Bookings

amount: Total payment amount

status: Payment status (e.g., paid, pending)

timestamp: Date and time of payment

### Relationships:

A payment is linked to one booking

A booking has one associated payment

### 🔄 Entity Relationships Summary:
One User can list many Properties

One User can make many Bookings

One Property can have many Bookings and Reviews

One Booking belongs to one User and one Property

One Booking has one Payment



