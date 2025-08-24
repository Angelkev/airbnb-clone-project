# airbnb-clone-project

# AirBnB Clone – Project

## Overview
This project is an educational, full-stack clone of core Airbnb features. It focuses on building a clean domain model, RESTful APIs, a responsive UI, and integrating authentication, persistence, and testing.

## Project Goals
- Model users, listings, availability, bookings, and reviews
- Implement secure authentication & authorization
- Build search & filtering for listings (location, dates, guests)
- Support booking flows and simple payments mock
- Ensure data persistence with migrations & validation
- Add automated tests and CI
- Package with Docker and deploy to a cloud host

## Tech Stack
- **Frontend:** React (Vite), React Router
- **Backend:** FastAPI (Python 3.x)
- **Database:** PostgreSQL + SQLAlchemy (Alembic for migrations)
- **Auth:** JWT-based auth
- **Testing:** Pytest, Vitest/RTL
- **DevOps:** Docker, GitHub Actions


## Team Roles

- **Backend Developer**: Responsible for building and maintaining the server-side logic, APIs, and integration with the database.
- **Frontend Developer**: Designs and implements the user interface and user experience of the application.
- **Database Administrator (DBA)**: Manages the database, ensures data integrity, performance, and security.
- **Project Manager**: Oversees the project, manages timelines, and coordinates between team members.
- **QA Engineer**: Tests the application to ensure quality, identifies bugs, and verifies fixes.


## Technology Stack

- **React**: A frontend JavaScript library used for building dynamic user interfaces and single-page applications.
- **FastAPI**: A Python web framework for building RESTful APIs quickly and efficiently.
- **PostgreSQL**: A relational database management system used to store all application data securely.
- **SQLAlchemy**: An ORM (Object Relational Mapper) for Python that allows easy database interaction using Python objects.
- **Alembic**: A database migration tool to handle schema changes over time.
- **JWT (JSON Web Tokens)**: Used for secure user authentication and authorization.
- **Docker & Docker Compose**: Containerization tools to package the application and its dependencies for easy deployment.
- **Pytest**: Python testing framework to write automated tests for backend functionality.
- **Vitest / React Testing Library**: Testing tools for frontend components and interactions.
- **Prettier & ESLint**: Code formatting and linting tools to maintain consistent code quality.
- **GitHub Actions**: CI/CD tool to automate test


## Database Design

### Key Entities and Fields

- **Users**
  - `id`: Unique identifier for each user
  - `name`: Full name of the user
  - `email`: Email address (used for login)
  - `password_hash`: Hashed password for authentication
  - `created_at`: Account creation timestamp

- **Properties**
  - `id`: Unique identifier for each property
  - `owner_id`: References the user who owns the property
  - `title`: Name/title of the property
  - `description`: Detailed description
  - `price_per_night`: Cost per night of stay

- **Bookings**
  - `id`: Unique identifier for each booking
  - `user_id`: Ref_


## Feature Breakdown

- **User Management**  
  Allows users to create accounts, log in, and manage their profile information. Includes authentication, authorization, and password security.

- **Property Management**  
  Enables property owners to add, edit, and delete listings. Owners can manage availability, pricing, and property details.

- **Booking System**  
  Lets users search for properties, make bookings, and manage reservations. Handles conflicts, availability, and booking statuses.

- **Review System**  
  Users can leave ratings and feedback on properties they have stayed in. Supports transparency and helps future users make informed decisions.

- **Payment Handling**  
  Integrates secure payment processing for completed bookings. Tracks payment status and ensures proper accounting.

- **Search & Filtering**  
  Users can search listings by location, dates, and number of guests. Provides filtering options to refine search results.


## API Security

- **Authentication**  
  Ensures that only registered users can access protected endpoints. Protects user accounts and personal information from unauthorized access.

- **Authorization**  
  Controls what each user is allowed to do based on their role (e.g., admin, property owner, guest). Prevents users from performing actions they shouldn’t have access to.

- **Rate Limiting**  
  Limits the number of requests a user or IP can make in a given time frame. Protects the server from abuse, denial-of-service attacks, and ensures fair usage.

- **Data Validation & Sanitization**  
  Checks and cleans incoming data to preve
