# 💻 SYNCCODE — Instant Coding Room

> A collaborative coding workspace designed to bring developers together for shared coding, learning, and problem-solving.

![Project](https://img.shields.io/badge/Project-SyncCode-blue)
![Architecture](https://img.shields.io/badge/Architecture-Client%20%2B%20Server-purple)
![Docker](https://img.shields.io/badge/Docker-Compose-2496ED?logo=docker&logoColor=white)
![Status](https://img.shields.io/badge/Status-Development-orange)
![License](https://img.shields.io/badge/License-Not%20Specified-lightgrey)

## 📖 Overview

**SYNCCODE — Instant Coding Room** is a collaborative coding project organized into separate client and server applications. Its repository includes the frontend, backend, and a Docker Compose configuration for running both components together.

The project provides a foundation for building an online coding room where developers can work together in a shared development environment.

By separating the client and server, the application maintains a modular structure that supports independent development, testing, and deployment of its components.

🔗 **Repository:** [SYNCCODE-INSTANT-CODING-ROOM](https://github.com/pratikabhang/SYNCCODE-INSTANT-CODING-ROOM)

## ✨ Features

- **Separate Client and Server:** Organizes the application into independently maintained frontend and backend components.
- **Docker Compose Integration:** Defines a multi-container development environment.
- **Modular Architecture:** Keeps client-side and server-side code in separate directories.
- **Dedicated Development Ports:** Exposes the client on port `5173` and the server on port `3000` through the provided Compose configuration.
- **Containerized Development:** Uses Dockerfiles in the client and server directories to build container images.
- **Extensible Foundation:** Provides a structure for developing and extending collaborative coding functionality.

Specific capabilities such as real-time synchronization, room creation, chat, authentication, and code execution should be documented only after confirming their implementation in the source code.

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Client application | Frontend interface |
| Server application | Backend functionality |
| Docker | Containerization |
| Docker Compose | Multi-container application orchestration |
| Git and GitHub | Version control and source hosting |

The exact programming languages, frontend framework, backend framework, and external dependencies should be confirmed from the source files and package manifests.

## 🏗️ Architecture

The application uses a client-server architecture with separate containers.

```text
                 Developer
                     |
                     v
                Web Browser
                     |
                     v
              Client Application
                 Port 5173
                     |
                     v
              Server Application
                 Port 3000
                     |
                     v
             Application Services
```

Docker Compose coordinates the client and server containers and connects them through a shared Docker bridge network.

### Main Components

| Component | Responsibility |
|---|---|
| `client/` | Frontend application |
| `server/` | Backend application |
| `client/Dockerfile` | Defines the client container build |
| `server/Dockerfile` | Defines the server container build |
| `docker-compose.yml` | Configures services, ports, volumes, and networking |
| `.gitignore` | Specifies files Git should ignore |
| `.github/ISSUE_TEMPLATE/` | Provides templates for repository issues |
| `.vscode/` | Contains editor-related project configuration |

## 🎯 Objectives

- Organize the application into distinct client and server components.
- Simplify local development with Docker Compose.
- Provide a maintainable foundation for collaborative coding functionality.
- Make the application easier to build, test, and extend.
- Support future improvements to the coding-room experience.

## 📂 Project Structure

```text
SYNCCODE-INSTANT-CODING-ROOM/
├── .github/
│   └── ISSUE_TEMPLATE/
├── .vscode/
├── client/
│   └── Dockerfile
├── server/
│   └── Dockerfile
├── docker-compose.yml
├── .gitignore
├── .gitattributes
└── preview.png
```

The client and server directories contain their respective application source files and supporting configuration.

## 💻 Prerequisites

Before running the project, install:

- [Git](https://git-scm.com/)
- [Docker Desktop](https://www.docker.com/products/docker-desktop/) or Docker Engine
- Docker Compose, included with current Docker Desktop installations

If you intend to run the client and server outside Docker, you may also need Node.js and npm. Confirm the required versions from the project's package manifests.

## 🚀 Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/pratikabhang/SYNCCODE-INSTANT-CODING-ROOM.git
cd SYNCCODE-INSTANT-CODING-ROOM
```

### 2. Review Configuration

Inspect the following files before starting the application:

- `docker-compose.yml`
- `client/Dockerfile`
- `server/Dockerfile`

Check whether the application requires environment variables, API credentials, or additional services. Configure them according to the actual application requirements.

### 3. Build and Start the Containers

From the repository root, run:

```bash
docker compose up --build
```

Docker Compose builds the client and server images and starts the configured services.

### 4. Open the Application

Once the client starts successfully, open:

**Client:** [http://localhost:5173](http://localhost:5173)

The server is exposed on:

**Server:** [http://localhost:3000](http://localhost:3000)

The server's exact routes and API endpoints depend on the implementation.

### 5. Stop the Application

To stop the containers, press `Ctrl+C` in the terminal and run:

```bash
docker compose down
```

### 6. View Container Logs

To inspect application output:

```bash
docker compose logs
```

To follow logs continuously:

```bash
docker compose logs -f
```

## ▶️ Usage

1. Start the client and server using Docker Compose.
2. Open the client URL in your browser.
3. Interact with the functionality implemented in the application.
4. Review the server logs if a request fails.
5. Stop the containers when finished.

The exact user workflow, including any room-creation or collaboration steps, should follow the controls and instructions implemented in the current application.

## 🧰 Development Workflow

### Rebuild After Configuration Changes

```bash
docker compose up --build
```

### Check Running Containers

```bash
docker compose ps
```

### Inspect Client Logs

```bash
docker compose logs -f client
```

### Inspect Server Logs

```bash
docker compose logs -f server
```

### Shut Down the Environment

```bash
docker compose down
```

## 🔐 Security Considerations

Before deploying the application publicly:

- Keep API keys, passwords, and other secrets out of source control.
- Configure environment variables securely.
- Validate and sanitize untrusted user input.
- Apply authentication and authorization where protected operations require them.
- Restrict access to backend endpoints as appropriate.
- Use HTTPS for public deployments.
- Review Docker configuration and dependencies before production use.

## 🔮 Future Enhancements

Potential enhancements for an instant coding-room application include:

- Real-time collaborative code editing.
- Shareable coding rooms and session links.
- Syntax highlighting and multi-language support.
- Integrated chat for participants.
- Code execution with appropriate sandboxing.
- User authentication and room access controls.
- Responsive interface improvements.
- Automated tests and continuous integration.
- Detailed API and deployment documentation.

These are possible future directions, not assertions that the features already exist.

## 🤝 Contributing

Contributions, bug reports, and suggestions are welcome.

1. Fork the repository.
2. Clone your fork:

   ```bash
   git clone https://github.com/<your-username>/SYNCCODE-INSTANT-CODING-ROOM.git
   cd SYNCCODE-INSTANT-CODING-ROOM
   ```

3. Create a feature branch:

   ```bash
   git checkout -b feature/your-feature-name
   ```

4. Make your changes in the appropriate client or server directory.
5. Test the changes and verify that the Docker environment starts correctly.
6. Commit your work:

   ```bash
   git add .
   git commit -m "Improve coding room functionality"
   ```

7. Push your branch:

   ```bash
   git push origin feature/your-feature-name
   ```

8. Open a pull request describing your changes and the tests performed.

## 📄 License

No repository-wide license has been confirmed. Until a `LICENSE` file is added, do not assume that the project may be freely redistributed or reused.

## 👨‍💻 Author

**Pratik Abhang**

- GitHub: [@pratikabhang](https://github.com/pratikabhang)
- Repository: [SYNCCODE-INSTANT-CODING-ROOM](https://github.com/pratikabhang/SYNCCODE-INSTANT-CODING-ROOM)

---

⭐ If you find this project useful, consider starring the repository.

*Build together. Code together. Learn together.*
