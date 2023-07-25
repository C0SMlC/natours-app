# Natours API and Website
Welcome to the Natours API and Website repository! This project serves as the backend API for the Natours website, which allows users to explore and book various nature tours. The API is built using Node.js, Express, and MongoDB. The API provides various endpoints to interact with tour data, user authentication, and more.

## Technologies Used
The Natours API and Website are built using the following technologies:

1 Node.js: A powerful JavaScript runtime environment that allows us to run server-side applications.
2 Express: A minimal and flexible Node.js web application framework used for building APIs and web applications.
3 MongoDB: A popular NoSQL database that stores data in JSON-like documents, providing flexibility and scalability.

## API Documentation
You can find the detailed API documentation [here](https://documenter.getpostman.com/view/26338834/2s946fdY5K). This documentation provides information about all the available endpoints, their input parameters, expected responses, and authentication requirements.

## Website
The Natours website can be accessed [here](https://natours-wlol.onrender.com/). It allows users to browse through a selection of nature tours, view details about each tour, and make bookings.

## JWT Token - How it Works
The Natours API uses JSON Web Tokens (JWT) for authentication. JWT is a compact and self-contained way of transmitting information between parties as a JSON object. In this application, JWT is used to verify the identity of users who want to access certain protected API endpoints.

## Authentication Flow
User Registration: When a new user registers on the Natours website, their credentials (e.g., username and password) are securely stored in the database.

1 User Login: To access protected API endpoints, the user needs to log in using their registered credentials. When the user sends a login request to the API, the server verifies the provided credentials against the stored data in the MongoDB database.

2 JWT Generation: If the provided credentials are valid, the server generates a JWT token with a secret key. This token contains information about the user and is signed with the secret key to ensure its authenticity.

3 Token Issuance: The server sends the generated JWT token back to the client (website) as part of the login response.

4 Subsequent Requests: For subsequent requests to protected API endpoints, the client needs to include the JWT token in the Authorization header of the HTTP request.

5 Token Verification: Upon receiving a request with a JWT token, the server verifies the token's signature and extracts the user information from it. If the token is valid and not expired, the server allows access to the protected resources.

## Installation
To run the Natours API and Website locally, follow these steps:

Clone the repository:
git clone (https://github.com/C0SMlC/natours-app/)
cd natour

Install dependencies for both the API and Website:
npm install

Set up the environment variables:

Rename .env.example to .env in both the api and website directories.
Modify the .env files and provide the required configurations, such as database connection URL, API secret key, etc.
Start the API server:

npm start
The API server should now be running on http://localhost:3000.
The Natours website should now be accessible at http://localhost:3000.

Please note that you need to have Node.js and MongoDB installed on your machine before running the application.

Contributing
Everyone is  welcome to contribute to the Natours API and Website project. If you find any issues or have suggestions for improvements, please feel free to open an issue or submit a pull request.

Happy coding!

The API and the Website is the part of [Jonas Schmedtmann's](https://www.udemy.com/user/jonasschmedtmann/) [Node.js, Express, MongoDB & More: The Complete Bootcamp 2023](https://www.udemy.com/course/nodejs-express-mongodb-bootcamp/) course.
