# Hotel Kong Arthur Microservices

*Description*: The Hotel Kong Arthur Microservices project is a scalable, modular, and distributed architecture for managing various operations of a hotel, such as guest information, reservations, room management, and reviews. Each microservice is independent, focusing on a specific domain and ensuring smooth communication and data consistency across services via an API Gateway.

---

## Table of Contents
- [Project Architecture](#project-architecture)
- [Microservices Overview](#microservices-overview)
- [Technologies Used](#technologies-used)
- [Getting Started](#getting-started)
- [Environment Variables](#environment-variables)
- [API Gateway](#api-gateway)
- [Running with Docker](#running-with-docker)
- [Testing](#testing)
- [Contributing](#contributing)
- [License](#license)

---

## Project Architecture

The system consists of multiple microservices, each responsible for a distinct domain within the hotel management system. This includes:

- *Guests*: Managing guest profiles and information.
- *Reservations*: Handling room reservations and availability.
- *Room Services*: Managing room inventory, types, and pricing.
- *Reviews*: Collecting and displaying guest reviews.

Each service is containerized with Docker, and an *API Gateway* provides a single entry point for clients, routing requests to the appropriate microservice based on the endpoint.

---

## Microservices Overview

| Service             | Port | Description                                         | Repository                                                              |
|---------------------|------|-----------------------------------------------------|-------------------------------------------------------------------------|
| *Guest Service*        | 5001 | Manages guest information and profile data        | [guest_service](https://github.com/Hotel-Kong-Arthur-Microservices/guest_service) |
| *Reservations Service* | 5002 | Manages reservations and booking operations       | [reservations_service](https://github.com/Hotel-Kong-Arthur-Microservices/reservations_service) |
| *Room Services*        | 5003 | Manages room inventory, availability, and pricing | [room_services](https://github.com/Hotel-Kong-Arthur-Microservices/room_services) |
| *Review Service*       | 5004 | Handles guest reviews and ratings                 | [hotel_reviews](https://github.com/Hotel-Kong-Arthur-Microservices/hotel_reviews) |

---

## Technologies Used

- *Programming Language*: Python
- *Framework*: Flask
- *Database*: SQLite (per microservice)
- *Containerization*: Docker, Docker Compose
- *Networking*: Docker Networking
- *API Gateway*: Flask-based Gateway for unified access

---

## Getting Started

### Prerequisites
Ensure you have the following installed:
- *Docker* and *Docker Compose*
- *Python 3.8+* (for local testing and development)

### Cloning the Repository
Clone the main project repository and each individual microservice repository:

git clone https://github.com/Hotel-Kong-Arthur-Microservices/main_repository
cd main_repository

Environment Variables

Each service requires specific environment variables for configuration, which can be defined in an .env file in each service directory. Example variables:
FLASK_APP=app.py
FLASK_ENV=development
DATABASE_URL=sqlite:///database.db
PORT=5001  # Different for each service
API Gateway

The API Gateway routes requests to the correct microservice. It is configured to listen on port 5000. Below are example routes:

Guests: http://localhost:5000/api/guests
Reservations: http://localhost:5000/api/reservations
Rooms: http://localhost:5000/api/rooms
Reviews: http://localhost:5000/api/reviews
Refer to each service's README for specific API routes and request details.
*Description*: The Hotel Kong Arthur Microservices project is a scalable, modular, and distributed architecture for managing various operations of a hotel, such as guest information, reservations, room management, and reviews. Each microservice is independent, focusing on a specific domain and ensuring smooth communication and data consistency across services via an API Gateway.

---

## Table of Contents
- [Project Architecture](#project-architecture)
- [Microservices Overview](#microservices-overview)
- [Technologies Used](#technologies-used)
- [Getting Started](#getting-started)
- [Environment Variables](#environment-variables)
- [API Gateway](#api-gateway)
- [Running with Docker](#running-with-docker)
- [License](#license)

---

## Project Architecture

The system consists of multiple microservices, each responsible for a distinct domain within the hotel management system. This includes:

- *Guests*: Managing guest profiles and information.
- *Reservations*: Handling room reservations and availability.
- *Room Services*: Managing room inventory, types, and pricing.
- *Reviews*: Collecting and displaying guest reviews.

Each service is containerized with Docker, and an *API Gateway* provides a single entry point for clients, routing requests to the appropriate microservice based on the endpoint.

---

## Microservices Overview

| Service             | Port | Description                                         | Repository                                                              |
|---------------------|------|-----------------------------------------------------|-------------------------------------------------------------------------|
| *Guest Service*        | 5001 | Manages guest information and profile data        | [guest_service](https://github.com/Hotel-Kong-Arthur-Microservices/guest_service) |
| *Reservations Service* | 5002 | Manages reservations and booking operations       | [reservations_service](https://github.com/Hotel-Kong-Arthur-Microservices/reservations_service) |
| *Room Services*        | 5003 | Manages room inventory, availability, and pricing | [room_services](https://github.com/Hotel-Kong-Arthur-Microservices/room_services) |
| *Review Service*       | 5004 | Handles guest reviews and ratings                 | [hotel_reviews](https://github.com/Hotel-Kong-Arthur-Microservices/hotel_reviews) |

---

## Technologies Used

- *Programming Language*: Python
- *Framework*: Flask
- *Database*: SQLite (per microservice)
- *Containerization*: Docker, Docker Compose
- *Networking*: Docker Networking
- *API Gateway*: Flask-based Gateway for unified access

---

## Getting Started

### Prerequisites
Ensure you have the following installed:
- *Docker* and *Docker Compose*
- *Python 3.8+* (for local testing and development)

### Cloning the Repository
Clone the main project repository and each individual microservice repository:

```bash
git clone https://github.com/Hotel-Kong-Arthur-Microservices/main_repository
cd main_repository
```

## Environment Variables

Each service requires specific environment variables for configuration, which can be defined in an .env file in each service directory. Example variables:

plaintext
Copy code
FLASK_APP=app.py
FLASK_ENV=development
DATABASE_URL=sqlite:///database.db
PORT=5001  # Different for each service
API Gateway

The API Gateway routes requests to the correct microservice. It is configured to listen on port 5000. Below are example routes:

Guests: http://localhost:5000/api/guests
Reservations: http://localhost:5000/api/reservations
Rooms: http://localhost:5000/api/rooms
Reviews: http://localhost:5000/api/reviews
Refer to each service's README for specific API routes and request details.

Running with Docker

The project uses Docker Compose to set up each microservice along with the API Gateway.

Steps to Build and Run
Build and Start Services:

```bash

docker-compose up --build
```

Access API Gateway:
Once all services are running, access the API Gateway at http://localhost:5000.
Shut Down:
```bash
docker-compose down
```

License

This project is licensed under the MIT License. See the LICENSE file for more details.
