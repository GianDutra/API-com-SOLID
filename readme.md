# Gym Pass API (SOLID)

<p align="center">
  <img alt="GitHub language count" src="https://img.shields.io/github/languages/count/GianDutra/Gym-Pass-API-SOLID?color=%2304D361">

   <a href="https://github.com/GianDutra/Gym-Pass-API-SOLID/commits/master">
    <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/GianDutra/Gym-Pass-API-SOLID">
  </a>
  
</p>
<img src="./.github/1.png" alt="Gym-Pass-API-SOLID" title="Gym-Pass-API-SOLID">



> This project was developed as part of the Rocketseat bootcamp, using SOLID principles and including end-to-end tests and unit tests.

## About the Project

The Gym Pass API is an application that allows users to check in at gyms. Additionally, it offers functionalities for user authentication, user profile management, and searching for nearby gyms. Below are the main requirements and functionalities:

### Functional Requirements

- [X] User registration
- [X] User authentication
- [X] Retrieval of the logged-in user's profile
- [X] Retrieval of the number of check-ins performed by the logged-in user
- [X] User check-in history
- [X] Search for nearby gyms (up to 10km)
- [X] Search for gyms by name
- [X] Check-in at a gym
- [X] Validation of check-in by administrators
- [X] Gym registration by administrators

### Business Rules

- The user cannot register with a duplicate email
- The user cannot perform more than one check-in on the same day
- The user can only check in if they are within 100m of the gym
- The check-in can only be validated up to 20 minutes after it is performed
- Check-in validation can only be done by administrators
- Gym registration can only be done by administrators

### Non-Functional Requirements

- The user's password is stored encrypted
- Application data is persisted in a PostgreSQL database
- All data lists are paginated, displaying 20 items per page
- User authentication is done through JSON Web Token (JWT)

## Routes

### `GET - /gyms/search`

Returns the list of gyms that match the search term.

### `GET - /gyms/nearby`

Returns the list of gyms near the user's location.

### `POST - /gyms`

Creates a new gym. Only administrators can access this route.

### `POST - /users`

Creates a new user.

### `POST - /sessions`

Authenticates a user and returns a JWT token.

### `PATCH - /token/refresh`

Refreshes the JWT token.

### `GET - /me`

Returns the profile of the authenticated user.

### `GET - /check-ins/history`

Returns the check-in history of the authenticated user.

### `GET - /check-ins/metrics`

Returns check-in metrics for the authenticated user.

### `POST - /gyms/:gymId/check-ins`

Performs a check-in at a gym.

### `PATCH - /check-ins/:checkInId/validate`

Validates a check-in. Only administrators can access this route.

## Technologies Used

- **[NodeJS](https://nodejs.org)**
- **[Fastify](https://github.com/fastify/fastify)**
- **[PostgreSQL](https://www.postgresql.org/)**
- **[JWT (JSON Web Token)](https://jwt.io/)**

## 🚀 Testing Gym-Pass-API

```bash
# Clone this repository
$ git clone https://github.com/your-username/Gym-Pass-API.git

# Access the project folder in your terminal
$ cd Gym-Pass-API

# Install the dependencies
$ npm install

# Run the application in developer mode
$ npm run dev

# Access the API
To test the routes and interact with the API, you can use a tool like Insomnia or Postman. Follow these steps:

1. Open Insomnia or Postman on your computer.

2. Create a new request for each API route you want to test (e.g., POST, GET, PUT, DELETE).

3. Set the request URL to http://localhost:3333, which is the default address where your API should be running.

4. Configure the request method and add any required headers or request body parameters according to the route you want to test.

```


---


## 👨‍💼 Author

<table>
  <tr>
    <td align="center">
      <a href="#">
        <img src="https://github.com/GianDutra.png" width="100px;" alt="Foto do Gian no GitHub"/><br>
        <sub>
          <b>Gian Dutra</b>
        </sub>
      </a>
    </td>
  </tr>
</table>



