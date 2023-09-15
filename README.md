# Simple-Web-Page
# Nginx and MongoDB Docker Compose Setup

This Docker Compose configuration sets up an Nginx web server with basic authentication and a MongoDB database with authentication enabled. It also includes a sample `index.html` file for the Nginx server.

## Prerequisites

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)


## Navigate to the project directory:
1. Navigate to the project directory:
   ```bash
   $ cd nginx-mongo-docker-compose
2. Create a **.htpasswd** file for basic authentication:
   ```bash
   $ htpasswd -c ./nginx/.htpasswd username
   Replace `username` with your desired username.
3. Customize the **index.html** file in the **nginx** directory to your liking.
4. Start the Docker containers:
   ```bash
   $ docker-compose up -d
5. Access the Nginx server at **http://localhost**. You will be prompted 
   for basic authentication using the credentials you specified in the 
   **.htpasswd** file.

6. The MongoDB container will be accessible from the Nginx service via the 
   **MONGO_HOST** environment variable.

## Directory Structure
- **docker-compose.yml**: Defines the services (Nginx and MongoDB) and their configurations.
- **nginx/**: Contains the Nginx specific files.
- **index.html**: Custom HTML content.
- **default.conf**: Nginx configuration with basic authentication.
- **.htpasswd**: File generated to store usernames and encrypted passwords.





