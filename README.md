# Assignment 5 instructions

1. Create the `.env` files in the respective directories based on the txt files submitted in canvas (for ./backend/ai-service, ./backend/user-service, ./backend/email-service, ./frontend, ./matching-service, ./mongodb-database)

1. Run `docker-compose build`

1. Run `docker-compose up`

1. Goto http://localhost:3000

# Getting Started with Docker for Development

1. Install docker at https://www.docker.com/

2. Start docker

3. Run `docker-compose up --build` to build and run images and containers

4. Note: this does not start the api-gateway. Follow the relevant `./gateway/README.md`

## Developer guide

As of the last update of this README, only the user-service and question-service have been dockerized. A respective `Dockerfile` has been created within each of their folders. This `Dockerfile` specifies the instructions in order to build the container, install the necessary node modules etc. 

To simplify the container building, a `docker-compose.yml` has been created in order to start both containers at once. This is achieved through running `docker compose build` and `docker compose up` to call both dockerfiles.

The api-gateway requires more work, see https://dev.to/naseef012/create-a-microservices-app-with-dockerized-express-api-gateway-1kf9 for more information.

## Finishing Development

When you are done with developing, kill the program (Ctrl^C) and run `docker compose down`. This cleans up local resources used by docker.

Note: For Mac users, this doesn't work and volumes will continue to pile up. Run `docker system prune -a --volumes` occasionally to remove the remaining volumes.