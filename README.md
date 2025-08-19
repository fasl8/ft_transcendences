# ft_transcendence 🏓

# 📋 Implemented Modules

##  🔧 Web
- **Major module: Use a Framework as Backend**
     - We used **Django** as our backend framework to structure the server-side logic, manage users and games, and organize routing and backend views.
- **Minor module: Use a Front-End Framework or Toolkit**
     - The frontend was styled using **Bootstrap** and custom **CSS** for layout, responsiveness, and interface components.
- **Minor module: Use a Database for the Backend**
     - We used **PostgreSQL** database implemented for storing user accounts, game history, statistics, match records, and persistent data management.
<div align="center">
  <img src="https://github.com/fasl8/ft_transcendences/blob/main/photo/1.homepage.png" alt="Homepage" width="600"/>
</div>


## 👥 User Management
<div align="center">
  <img src="https://github.com/fasl8/ft_transcendences/blob/main/photo/6.gamehub.png" alt="gamehub" width="600"/>
</div>

- **Major module: Standard User Management, Authentication, Users Across Tournaments**
     - Users can subscribe to the website securely
          <div align="center">
              <img src="https://github.com/fasl8/ft_transcendences/blob/main/photo/4.signup.jpeg" alt="Homepage" width="600"/>
          </div>

     - Registered users can log in with secure authentication

          <div align="center">
            <img src="https://github.com/fasl8/ft_transcendences/blob/main/photo/5.signin.png" alt="Signin" width="600"/>
          </div>

     - Users can select unique display names for tournaments
 
          <div align="center">
            <img src="https://github.com/fasl8/ft_transcendences/blob/main/photo/10.nickname.png" alt="nickname" width="600"/>
          </div>   

          <div align="center">
            <img src="https://github.com/fasl8/ft_transcendences/blob/main/photo/27.tournament.png" alt="tournament" width="600"/>
          </div>           
     - Profile management with information updates

          <div align="center">
            <img src="https://github.com/fasl8/ft_transcendences/blob/main/photo/8.setting.png" alt="setting" width="600"/>
          </div>

          <div align="center">
            <img src="https://github.com/fasl8/ft_transcendences/blob/main/photo/11.password.png" alt="password" width="600"/>
          </div>

       <div align="center">
            <img src="https://github.com/fasl8/ft_transcendences/blob/main/photo/33.delet.png" alt="delet1" width="600"/>
          </div> 

       <div align="center">
            <img src="https://github.com/fasl8/ft_transcendences/blob/main/photo/12.delet.png" alt="delet2" width="600"/>
          </div> 
  
     - Avatar upload system with default options
  
          <div align="center">
            <img src="https://github.com/fasl8/ft_transcendences/blob/main/photo/18.profilewfms.png" alt="Profilewfms" width="600"/>
          </div>
  
     - Friend system
          <div align="center">
            <img src="https://github.com/fasl8/ft_transcendences/blob/main/photo/30.friendaccess.png" alt="friend1" width="600"/>
          </div>

          <div align="center">
            <img src="https://github.com/fasl8/ft_transcendences/blob/main/photo/31.friendaccess.png" alt="friend2" width="600"/>
          </div>
          
     - User profiles displaying stats (wins/losses)
     - Match History including 1v1 games, dates, and detailed records
  
     
- **Major module: Implementing Remote Authentication**
     - We implemented **OAuth 2.0 authentication with 42 intra website**, allowing students to sign in securely using their 42Account.

## 🎮 Gameplay and User Experience
<div align="center">
       <img src="https://github.com/fasl8/ft_transcendences/blob/main/photo/20.menu.png" alt="menu" width="600"/>
     </div>
     
- **Major module: Multiplayers (more than 2 in the same game)**
    - Our platform supports a 6-player Pong game played in real time on a circular arena. Each player controls a paddle positioned along the edge of the circle. The ball bounces within the circular space, requiring players to anticipate angles and coordinate in a competitive, fast-paced environment. This setup adds a unique and dynamic twist to the classic Pong gameplay.

     <div align="center">
       <img src="https://github.com/fasl8/ft_transcendences/blob/main/photo/26.multboard.png" alt="multboard" width="600"/>
     </div>
            
## 🤖 AI & Algorithm
- **Major module: Introduce an AI Opponent**
    - A custom AI opponent was developed using reactive logic to simulate human gameplay. The AI refreshes its view of the game once per second, anticipates ball movement, and can win against real players. The AI plays fairly, with the same speed and rules as human players.

     <div align="center">
       <img src="https://github.com/fasl8/ft_transcendences/blob/main/photo/21.ai.png" width="600"/>
     </div>

     <div align="center">
       <img src="https://github.com/fasl8/ft_transcendences/blob/main/photo/25.pingpong.png" width="600"/>
     </div> 
- **Minor module: User and Game Stats Dashboards**
    - We created detailed dashboards: showing win/loss stats, match history, Performance history over time, and game records(Scores from games, Game type, Date and time of each match).These dashboards use simple visual elements and charts to give users clear insight into their gameplay activity..
          <div align="center">
            <img src="https://github.com/fasl8/ft_transcendences/blob/main/photo/32.fullpagedash.png" alt="Dashboard" width="600"/>
          </div>
   

## 🔐 Cybersecurity
- **Major module: Implement Two-Factor Authentication (2FA) and JWT**
    - We implemented **Two-Factor Authentication** via email-based OTP for secure login and **JSON Web Tokens (JWT)**  to manage user sessions securely. All user inputs are validated, and **HTTPS** is enforced to ensure secure communication across the entire website.
          <div align="center">
            <img src="https://github.com/fasl8/ft_transcendences/blob/main/photo/9.enable2fa.png" alt="enable2fa" width="600"/>
          </div>
          <div align="center">
            <img src="https://github.com/fasl8/ft_transcendences/blob/main/photo/29.disable2fa.png" alt="disable2fa" width="600"/>
          </div>
          <div align="center">
            <img src="https://github.com/fasl8/ft_transcendences/blob/main/photo/28.code.png" alt="2FA" width="600"/>
          </div>

## ⚙️ DevOps
- **Major module: Designing the Backend as Microservices**
    - We split the project into three Dockerized microservices, and each one contains both frontend and backend parts with a sprite-based structure:
    - **gamehub**: Authentication, user accounts, and game statistics management
    - **gameplay**: Game logic, matchmaking, and real-time player coordination
    - **home**: Landing page and general website content
  - Each microservice containerized using **Docker**
     - **Docker Compose** orchestration for easy deployment
     - **NGINX** configured as reverse proxy for traffic routing and HTTPS enforcement
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
  - All services are containerized using Docker, and we use Docker Compose to orchestrate and run the entire system with a single command.
  - We configured NGINX as a reverse proxy to route traffic securely to each service and enforce HTTPS across the entire platform. NGINX also manages caching and performance optimizations between containers.

## 🌍 Accessibility
- **Minor module: Multiple Language Support**
    - We implemented a dynamic language switcher supporting English and Arabic, with translated labels, buttons, and user content using JavaScript localization.
          <div align="center">
            <img src="https://github.com/fasl8/ft_transcendences/blob/main/photo/7.language.png" alt="language" width="600"/>
          </div>
- **Minor module: Server-Side Rendering (SSR) Integration**
    - Parts of the app are rendered server-side using Django templates to support SEO and improve performance on slower networks.

## 👥 Team Members

- [W](https://github.com/wadha655)  
- [F](https://github.com/fasl8)
- [M](https://github.com/malmessa42)  
- [S](https://github.com/Saalamoo)  

## 🤝 Contributing

This project follows 42 University guidelines and standards. All implementation decisions are justified and documented for evaluation purposes.
**Built according to ft_transcendence subject requirements v14.2**


## 📝 License

This project is part of the 42 University curriculum and adheres to the university academic policies.
