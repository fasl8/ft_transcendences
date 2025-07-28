# ft_transcendence 🏓

# 📋 Implemented Modules

##  🔧 Web
  -  Major module: Use a Framework as Backend
      * We used Django as our backend framework to structure the server-side logic, manage users and games, and organize routing and backend views.
  -  Minor module: Use a Front-End Framework or Toolkit
      * The frontend was styled using Bootstrap and custom CSS for layout, responsiveness, and interface components. No advanced frontend frameworks were used.
  -  Minor module: Use a Database for the Backend
      * We used PostgreSQL for storing user accounts, game history, stats, and game records.
<div align="center">
  <img src="https://github.com/fasl8/ft_transcendences/blob/main/photo/1.homepage.png" alt="Homepage" width="600"/>
</div>


## 👥 User Management
  -  Major module: Standard User Management, Authentication, Game Records
      - Users can subscribe to the website securely
          <div align="center">
              <img src="https://github.com/fasl8/ft_transcendences/blob/main/photo/4.signup.jpeg" alt="Homepage" width="600"/>
          </div>

      - Registered users can log in with secure authentication
  
          <div align="center">
            <img src="https://github.com/fasl8/ft_transcendences/blob/main/photo/5.signin.png" alt="Signin" width="600"/>
          </div>

      - Users can select unique display names for tournaments
      - Profile management with information updates
          <div align="center">
            <img src="https://github.com/fasl8/ft_transcendences/blob/main/photo/8.setting.png" alt="setting" width="600"/>
          </div>
      - Avatar upload system with default options
          <div align="center">
            <img src="https://github.com/fasl8/ft_transcendences/blob/main/photo/18.profilewfms.png" alt="Profilewfms" width="600"/>
          </div>
      - Friend system
      - User profiles displaying stats (wins/losses)
      - Match History including 1v1 games, dates, and detailed records
          <div align="center">
            <img src="https://github.com/fasl8/ft_transcendences/blob/main/photo/32.fullpagedash.png" alt="Dashboard" width="600"/>
          </div>        
  - Major module: Implementing Remote Authentication
       - We implemented OAuth2 login with 42 intra, allowing students to sign in securely using their 42Account.

## 🎮 Gameplay and User Experience
  - Major module: Multiplayers (more than 2 in the same game)
    - Our platform supports a 6-player Pong game played in real time on a circular arena. Each player controls a paddle positioned along the edge of the circle. The ball bounces within the circular space, requiring players to anticipate angles and coordinate in a competitive, fast-paced environment. This setup adds a unique and dynamic twist to the classic Pong gameplay.

## 🤖 AI & Algorithm
  - Major module: Introduce an AI Opponent
    - A custom AI opponent was developed using reactive logic to simulate human gameplay. The AI refreshes its view of the game once per second, anticipates ball movement, and can win against real players. The AI plays fairly, with the same speed and rules as human players.
  - Minor module: User and Game Stats Dashboards
    - We created detailed dashboards: showing win/loss stats, match history, Performance history over time, and game records(Scores from games, Game type, Date and time of each match).These dashboards use simple visual elements and charts to give users clear insight into their gameplay activity..
   

## 🔐 Cybersecurity
  - Major Module: Implement Two-Factor Authentication (2FA) and JWT
    - We implemented 2FA via email-based OTP for secure login and JWT tokens to manage user sessions securely. All user inputs are validated, and HTTPS is enforced to ensure secure communication across the entire website.
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
  - Major module: Designing the Backend as Microservices
    - We split the project into three Dockerized microservices, and each one contains both frontend and backend parts with a sprite-based structure:
        - gamehub – manages authentication, user accounts, and game stats
        - gameplay – handles game logic, matchmaking, and player coordination
        - home – serves the landing page and general website content
  - All services are containerized using Docker, and we use Docker Compose to orchestrate and run the entire system with a single command.
  - We configured NGINX as a reverse proxy to route traffic securely to each service and enforce HTTPS across the entire platform. NGINX also manages caching and performance optimizations between containers.

## 🌍 Accessibility
  - Minor module: Multiple Language Support
    - We implemented a dynamic language switcher supporting English and Arabic, with translated labels, buttons, and user content using JavaScript localization.
          <div align="center">
            <img src="https://github.com/fasl8/ft_transcendences/blob/main/photo/7.language.png" alt="language" width="600"/>
          </div>
  - Minor module: Server-Side Rendering (SSR) Integration
    - Parts of the app are rendered server-side using Django templates to support SEO and improve performance on slower networks.

## 🤝 Contributing

This project follows 42 School guidelines and standards. All implementation decisions are justified and documented for evaluation purposes.
**Built according to ft_transcendence subject requirements v14.2**


## 📝 License

This project is part of the 42 School curriculum and adheres to the school's academic policies.
