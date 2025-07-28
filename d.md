
### 🔧 Web Modules
- **Major module: Use a Framework as Backend**
  - **Django** framework used for backend development, handling server-side logic, user management, game coordination, and API endpoints.

- **Minor module: Use a Front-End Framework or Toolkit**
  - **Bootstrap** toolkit integrated for responsive design, UI components, and consistent styling across the platform.

- **Minor module: Use a Database for the Backend**
  - **PostgreSQL** database implemented for storing user accounts, game history, statistics, match records, and persistent data management.

### 👥 User Management Modules
- **Major module: Standard User Management, Authentication, Users Across Tournaments**
  - Users can subscribe to the website securely
  - Registered users can log in with secure authentication
  - Users can select unique display names for tournaments
  - Profile management with information updates
  - Avatar upload system with default options
  - Friend system with online status visibility
  - User profiles displaying stats (wins/losses)
  - Match History including 1v1 games, dates, and detailed records


- **Major module: Implementing Remote Authentication**
  - **OAuth 2.0 authentication with 42** integrated
  - Secure sign-in using 42 intranet credentials
  - User-friendly login and authorization flows
  - Secure token exchange between web application and 42 authentication provider

### 🎮 Gameplay and User Experience Modules
- **Major module: Multiplayers (more than 2 in the same game)**
  - **6-player Pong game** implemented with circular arena design
  - Real-time multiplayer coordination with live controls
  - Each player controls a paddle positioned around the circle's edge
  - Dynamic ball physics within circular space requiring strategic positioning

### 🤖 AI-Algo Modules
- **Major module: Introduce an AI Opponent**
  - Custom AI opponent developed with reactive logic
  - AI simulates human behavior with keyboard input simulation
  - Constraint: AI refreshes game view once per second, requiring ball movement anticipation
  - Intelligent decision-making that can win against real players
  - Fair play implementation with same speed and rules as human players

- **Minor module: User and Game Stats Dashboards**
  - Comprehensive dashboards showing win/loss statistics
  - Match history with detailed game records
  - Performance tracking over time with visual elements
  - Game records including scores, game types, dates and timestamps
  - User-friendly interface for accessing gaming history and metrics

### 🔐 Cybersecurity Modules
- **Major module: Implement Two-Factor Authentication (2FA) and JWT**
  - **Two-Factor Authentication** implemented via email-based OTP system
  - **JSON Web Tokens (JWT)** for secure session management
  - Additional security layer for user account protection
  - Secure authentication and authorization processes

### ⚙️ DevOps Modules
- **Major module: Designing the Backend as Microservices**
  - Backend architected using microservices approach with three specialized services:
    - **gamehub**: Authentication, user accounts, and game statistics management
    - **gameplay**: Game logic, matchmaking, and real-time player coordination
    - **home**: Landing page and general website content
  - Each microservice containerized using **Docker**
  - **Docker Compose** orchestration for easy deployment
  - **NGINX** configured as reverse proxy for traffic routing and HTTPS enforcement

## 🏗️ Technical Architecture

### Microservices Structure
```
┌─────────────┐    ┌─────────────┐    ┌─────────────┐
│   gamehub   │    │  gameplay   │    │    home     │
│             │    │             │    │             │
│ • Auth      │    │ • Game      │    │ • Landing   │
│ • Users     │    │   Logic     │    │   Page      │
│ • Stats     │    │ • Match     │    │ • General   │
│ • Records   │    │   Making    │    │   Content   │
└─────────────┘    └─────────────┘    └─────────────┘
```

### Technology Stack
- **Backend**: Django framework with PostgreSQL database
- **Frontend**: Bootstrap toolkit with custom CSS
- **Authentication**: OAuth 2.0 (42 integration) + JWT + 2FA
- **Infrastructure**: Docker containerization, Docker Compose orchestration
- **Reverse Proxy**: NGINX with HTTPS enforcement
- **Architecture**: Microservices design pattern

## 🎯 Game Features

### Revolutionary 6-Player Circular Pong
- Players positioned around circular arena perimeter
- Real-time multiplayer coordination
- Advanced ball physics with realistic circular bouncing
- Strategic gameplay requiring anticipation and positioning
- Fast-paced competitive environment

### Intelligent AI Opponent
- Human-like behavior simulation with keyboard input replication
- Strategic ball movement anticipation (1-second refresh constraint)
- Capable of winning against human players
- Fair play with identical speed and rules as human players

### Comprehensive User System
- Secure registration and authentication
- 42 OAuth integration for seamless login
- Profile management with avatar uploads
- Friend system with online status
- Detailed match history and statistics
- Two-factor authentication for enhanced security

## 🛠️ Installation & Setup

### Prerequisites
- Docker and Docker Compose installed
- Git for repository cloning

### Quick Start
```bash
# Clone the repository
git clone https://github.com/fasl8/ft_transcendences.git
cd ft_transcendences

# Launch all services with single command
docker-compose up --build

# Access the application
open https://localhost
```

### Security Features
- Password hashing for all stored credentials
- SQL injection and XSS protection
- HTTPS enforcement across entire platform
- Form validation on all user inputs
- JWT token-based session security
- Two-factor authentication via email OTP

## 🔒 Security Implementation

- **Password Security**: All passwords hashed using strong algorithms
- **SQL Injection Protection**: Parameterized queries and input sanitization
- **XSS Prevention**: Input validation and output encoding
- **HTTPS Enforcement**: SSL/TLS encryption for all communications
- **Session Security**: JWT tokens with proper expiration and validation
- **Two-Factor Authentication**: Email-based OTP for additional security layer


