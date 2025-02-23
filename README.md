[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/6BOvYMwN)
# PeerPrep 
## Getting Started with Docker for Development

1. Install docker at https://www.docker.com/

2. Start docker

3. For `frontend`, `ai-service`, `email-service`, `mongodb-database`, `user-service`, there is an `.env` file that is required. 
    Follow the respective `README.md` located in those folders.

4. Run `docker-compose up --build` to build and run images and containers

## Developer guide

As of the last update of this README, all backend services, frontend and gateway have been dockerized. A respective `Dockerfile` has been created within each of folders. This `Dockerfile` specifies the instructions in order to build the container, install the necessary node modules etc. 

To simplify the container building, a `docker-compose.yml` has been created in order to start both containers at once. This is achieved through running `docker-compose up --build` to call all the dockerfiles.

Note that user-service requires a Supabase database and question-service requires a MongoDB database. The respective `README.md` should aid you in creating your own databases.

Also, the ai-service requires your own OpenAI key and email-service requires an SMTP_PASSWORD to run locally. 

## General Guide

For more in-depth details on how this project was designed, view the [Final Report](https://github.com/CS3219-AY2324S1/ay2324s1-course-assessment-g58/blob/41c7c542916a343a0213b01d0a0704dc00a334b1/Group%2058%20Final%20Report.pdf)

## Finishing Development

When you are done with developing, kill the program (Ctrl^C) and run `docker compose down`. This cleans up local resources used by docker.

Note: For Mac users, this doesn't work and volumes will continue to pile up. Run `docker system prune -a --volumes` occasionally to remove the remaining volumes.
