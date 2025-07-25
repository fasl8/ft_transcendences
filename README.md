# ft_transcendences

- 🔧 Web
  -  Major module: Use a Framework as Backend
    - We used Django as our backend framework to structure the server-side logic, manage users and games, and organize routing and backend views.
  -  Minor module: Use a Front-End Framework or Toolkit
    - The frontend was styled using Bootstrap and custom CSS for layout, responsiveness, and interface components. No advanced frontend frameworks were used.
  -  Minor module: Use a Database for the Backend
    - We used PostgreSQL for storing user accounts, game history, stats, and game records.

- 👥 User Management
  -  Major module: Standard User Management, Authentication, Game Records
    - Users can register, log in securely, upload avatars, manage profiles, view game records and match history, and add friends. The system includes display name selection, profile stats, and player connections.
  - Major module: Implementing Remote Authentication
    - We implemented OAuth2 login with 42 intra, allowing students to sign in securely using their 42Account.

🎮 Gameplay and User Experience
  - Major module: Multiplayers (more than 2 in the same game)
    - Our platform supports a 6-player Pong game played in real time on a circular arena. Each player controls a paddle positioned along the edge of the circle. The ball bounces within the circular space, requiring players to anticipate angles and coordinate in a competitive, fast-paced environment. This setup adds a unique and dynamic twist to the classic Pong gameplay.

🤖 AI & Algorithm
  - Major module: Introduce an AI Opponent
    - A custom AI opponent was developed using reactive logic to simulate human gameplay. The AI refreshes its view of the game once per second, anticipates ball movement, and can win against real players. The AI plays fairly, with the same speed and rules as human players.
  - Minor module: User and Game Stats Dashboards
    - We created detailed dashboards: showing win/loss stats, match history, Performance history over time, and game records(Scores from games, Game type, Date and time of each match).These dashboards use simple visual elements and charts to give users clear insight into their gameplay activity..
   

🔐 Cybersecurity
  - Major Module: Implement Two-Factor Authentication (2FA) and JWT
    - We implemented 2FA via email-based OTP for secure login and JWT tokens to manage user sessions securely. All user inputs are validated, and HTTPS is enforced to ensure secure communication across the entire website.


⚙️ DevOps
  - Major module: Designing the Backend as Microservices
    - We split the project into three Dockerized microservices, and each one contains both frontend and backend parts with a sprite-based structure:
        - gamehub – manages authentication, user accounts, and game stats
        - gameplay – handles game logic, matchmaking, and player coordination
        - home – serves the landing page and general website content
  - All services are containerized using Docker, and we use Docker Compose to orchestrate and run the entire system with a single command.
  - We configured NGINX as a reverse proxy to route traffic securely to each service and enforce HTTPS across the entire platform. NGINX also manages caching and performance optimizations between containers.
