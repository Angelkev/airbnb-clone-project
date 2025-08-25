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

## Project Roles and Responsibilities

- **Project Manager**  
  Oversees the project timeline, coordinates team members, manages resources, and ensures milestones are met. Keeps the team aligned with project goals.

- **Frontend Developers**  
  Design and implement the user interface and user experience. Responsible for building responsive pages, integrating with backend APIs, and ensuring smooth interactions.

- **Backend Developers**  
  Develop and maintain server-side logic, APIs, and database integration. Ensure performance, scalability, and security of backend services.

- **Designers (UI/UX)**  
  Plan and create visual designs, wireframes, and prototypes. Focus on user-friendly interfaces and enhancing usability throughout the application.

- **QA/Testers**  
  Test application features for bugs, usability issues, and performance. Ensure the application meets quality standards before deployment.

- **DevOps Engineers**  
  Handle deployment pipelines, continuous integration/continuous deployment (CI/CD), and cloud infrastructure. Ensure smooth deployment and maintain system reliability.

- **Product Owner**  
  Defines project requirements, prioritizes features, and ensures the development aligns with business goals. Acts as a bridge between stakeholders and the development team.

- **Scrum Master**  
  Facilitates Agile ceremonies, removes blockers for the team, and ensures the development process follows Scrum methodology. Promotes productivity and collaboration.


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

## UI/UX Design Planning

### Design Goals
- Create an intuitive and responsive interface for both desktop and mobile users.
- Make navigation simple and consistent across all pages.
- Highlight key actions like searching, booking, and reviewing properties.
- Ensure accessibility and readability for all users.

### Key Features
- Search and filter properties easily by location, date, and guest count.
- Display property details including photos, description, amenities, and pricing.
- Enable smooth booking workflow with a simple checkout process.
- Allow users to view their bookings and leave reviews effortlessly.

### Primary Pages

| Page Name                | Description                                                                 |
|---------------------------|-----------------------------------------------------------------------------|
| **Property Listing View** | Shows a list of available properties with filters, sorting options, and key details like price and location. |
| **Listing Detailed View** | Displays detailed information for a selected property, including photos, amenities, host information, and reviews. |
| **Simple Checkout View**  | Provides a streamlined checkout process for booking a property, including date selection, payment details, and confirmation. |

### Importance of User-Friendly Design
A user-friendly design is crucial in a booking system because it improves usability, reduces errors, and increases customer satisfaction. Clear navigation, simple forms, and responsive layouts ensure that users can search, book, and manage reservations effortlessly, which leads to higher engagement and conversions.


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


## CI/CD Pipeline

Continuous Integration (CI) and Continuous Deployment (CD) are practices that automate testing, building, and deploying the application. CI/CD ensures that new code changes are automatically tested and deployed, reducing bugs and improving overall development efficiency.

**Key Benefits for this Project:**
- **Automated Testing:** Every code change is tested automatically to catch errors early.  
- **Consistent Deployments:** Ensures the application is deployed reliably across environments.  
- **Faster Iterations:** Reduces manual steps, allowing faster delivery of new features and bug fixes.

**Tools Used:**
- **GitHub Actions:** Automates workflows for testing, building, and deploying the application.  
- **Docker & Docker Compose:** Containerizes the application for consistent deployment in any environment.  
- **Optional CI/CD Tools:** Tools like Jenkins or GitLab CI could also be used for larger workflows.
