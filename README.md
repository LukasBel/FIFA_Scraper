# 2026 FIFA World Cup Ticket WebScraper

![FifaWebScraper](https://github.com/LukasBel/FIFA_Scraper/assets/45898249/6b376b61-0665-47e0-8120-87768822603e)

This project is a FIFA Ticket WebScraper designed to monitor the status of tickets and notify users via email when tickets 
go on sale or when there are updates regarding ticket availability. The project consists of a frontend built with **Vue.js** 
for a friendly graphical user interface (GUI), a backend written in **Go**, and a **PostgreSQL** database. The communication 
between the frontend and backend is established using CORS, and the backend utilizes the **Fiber** framework.

## Features

- Friendly GUI: The frontend provides a user-friendly interface for users to enter their email and submit it for ticket notifications.
- CORS: Cross-Origin Resource Sharing (CORS) is implemented to allow communication between the frontend and backend, even if they are hosted on different domains.
- PostgreSQL: The database management system used for storing user email addresses and other relevant data.
- Fiber: A web framework written in Go, Fiber is used for building the backend server and handling HTTP requests efficiently.

## How to Use

1. Clone the repository to your local machine.
2. Navigate to the project directory.
3. Install dependencies for both frontend and backend.
4. Start the backend server.
5. Start the frontend server.
6. Access the frontend in your web browser.

## Installation

### Backend (Go)

1. Navigate to the `backend` directory.
2. Run `go mod tidy` to install dependencies.
3. Configure the `.env` file with your PostgreSQL database credentials.
4. Run `go run main.go` to start the backend server.

### Frontend (Vue.js)

1. Navigate to the `frontend` directory.
2. Run `npm install` to install dependencies.
3. Run `npm run serve` to start the frontend server.

## Configuration

Ensure that you have PostgreSQL installed and running on your system. Configure the `.env` file in the backend directory with the necessary database credentials.

## Contributions

Contributions are welcome! Feel free to submit issues or pull requests to improve the project.

