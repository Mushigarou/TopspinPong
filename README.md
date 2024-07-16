# TopspinPong

- Play Ping Pong matches and tournaments, and chat live with your friends!

## Index

- [Technology Stack](#technology-stack)
- [Usage](#usage)
- [Merise](#merise)
- [Unified Modeling Language](#unified-modeling-language)
- [Features](#features)
- [Ressources](#ressources)

# Technology Stack

| Category               | Technology                                                                                                                                                                                                                                                                                                           |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Server**             | ![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)                                                                                                                                                                                                                     |
| **Backend Framework**  | ![Django REST](https://img.shields.io/badge/django%20rest-ff1709?style=for-the-badge&logo=django&logoColor=white)                                                                                                                                                                                                     |
| **Database**           | ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)                                                                                                                                                                                                     |
| **Containerization**   | ![Docker](https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker&logoColor=white)                                                                                                                                                                                                                  |
| **Frontend**           | ![Next.js](https://img.shields.io/badge/next%20js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white) ![Bootstrap](https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white) ![Three.js](https://img.shields.io/badge/ThreeJs-black?style=for-the-badge&logo=three.js&logoColor=white) |
| **Authentication**     | ![JWT](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=JSON%20web%20tokens&logoColor=white)                                                                                                                                                                                                           |
| **Monitoring and Logging** | ![Grafana](https://img.shields.io/badge/grafana-%23F46800.svg?style=for-the-badge&logo=grafana&logoColor=white) ![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=Prometheus&logoColor=white) ![Kibana](https://img.shields.io/badge/Kibana-005571?style=for-the-badge&logo=Kibana&logoColor=white) ![Elasticsearch](https://img.shields.io/badge/Elastic_Search-005571?style=for-the-badge&logo=elasticsearch&logoColor=white) |
| **Languages**          | ![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white) ![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white) ![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white) ![Python](https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue) |
| **Development Tools**  | ![VSCode](https://img.shields.io/badge/VSCode-0078D4?style=for-the-badge&logo=visual%20studio%20code&logoColor=white) ![Google Chrome](https://img.shields.io/badge/Google_chrome-4285F4?style=for-the-badge&logo=Google-chrome&logoColor=white) ![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white) |
| **Design**             | ![Figma](https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white)                                                                                                                                                                                                                     |

---

## Usage

```bash
# to see all available commands
$> make

# build images and run containers
$> make start

# to build docker images
$> make build

# to run docker containers
$> make up

# removes containers, volumes... and restart everything
$> make re

# generating some users and matches
$> make data-generator

```

**After running all the containers, you can access <a href='https://localhost' target="_blank">https://localhost</a>**

---

## Merise

### Logical Data Model

![Logical Data Model](docs/data_model.pgerd.png)


[⬆️ Back To Features](#supported-features)

---

## Unified Modeling Language

### Use Case

![Use Case](docs/use_case.drawio.png)
<!-- <img src="docs/use_case.drawio.png"> -->

- **Sign Up**: This use case allows a new user to create an account on the website. Users will provide necessary information such as username, email, and password to register themselves.
- **Sign In**: This use case enables registered users to authenticate themselves into the system by providing their username/email and password.
- **Dashboard**: Upon signing in, users are directed to their dashboard. The dashboard provides an overview of the user's profile, activities, notifications, and other relevant information.
- **Play Game**: Users can engage in playing games available on the website. This use case allows users to select and participate in various games, such as ping pong, available on the platform.
- **Chat**: Users can communicate with each other through the chat feature provided by the website. This use case enables users to send and receive messages, emojis, and other media in real-time.
- **View Achievement**: Users can view their achievements and milestones attained while using the website. This use case allows users to track their progress and accomplishments within the platform.
- **Logout**: This use case allows users to securely log out of their account, ensuring the privacy and security of their data.
- **Add Friends**: Users can expand their social network by adding other users as friends. This use case enables users to send and accept friend requests, thereby connecting with each other on the platform.
- **View Leaderboard**: Users can view the leaderboard to see rankings based on various criteria, such as game scores, achievements, or activity levels. This use case provides users with a sense of competition and allows them to compare their performance with others.
- **Update Profile**: Users can modify and update their profile information as needed. This use case allows users to edit their profile details, such as username, profile picture, bio, and other preferences.
- **Manage User Accounts**: Admins can manage user accounts, including creating new accounts, updating user information, and deactivating or deleting accounts if necessary.
- **Manage Admin Functions**: Admins have access to additional functionalities for managing the website, such as managing system settings, controlling access permissions, and handling reported issues or disputes.

[⬆️ Back To Features](#supported-features)

---


# Features

| Area | What it does |
|---|---|
| **Game** | Live Pong in the browser, 3D graphics with Three.js/WebGL, custom game options, remote players over WebSockets |
| **Tournaments** | Aliases per tournament, matchmaking and announcements for the next match |
| **Users** | Sign-up and login, OAuth 2.0 single sign-on, avatars, friends and online status, profile stats and match history |
| **Chat** | Direct messages, blocking, game invites from the chat, tournament notifications |
| **Stats** | Dashboards with charts for each player and each game |
| **Security** | Two-factor authentication (2FA), JWT, hashed passwords, input validation, HTTPS and WSS everywhere |
| **Backend** | Django REST API with PostgreSQL |
| **DevOps** | One-command start with Docker Compose, ELK stack for logs, Prometheus and Grafana for monitoring |

The site is a single-page application: the browser's Back and Forward buttons work as expected.

[⬆️ Back to top](#index)

## Ressources

- [NextJS and Cloudinary — App Router Integration](https://medium.com/@varchasvipandey/nextjs-and-cloudinary-app-router-integration-ad7fd2e0fdb2)
- [NextJS 13 API Routes: Better Than Expected!](https://www.youtube.com/watch?v=vrR4MlB7nBI&ab_channel=Joshtriedcoding)
