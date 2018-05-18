# Mongo container

MongoDB container with permanent db storage and mongo-express

## Docker Compose

This container uses **Docker-compose**:
Compose is a tool for defining and running complex applications with Docker. With Compose, you define a multi-container application in a single file, then spin your application up in a single command which does everything that needs to be done to get it running.

To make the project up and running go to the project main folder into the terminal and type:

 `$sudo docker-compose up`

**Docker-compose** will build the containers necessary for your environment. Basically there will be two containers: one with **Mongo** and one with **Mongo Express**.

## Mongo Express

[Mongo Express](https://github.com/mongo-express/mongo-express) is a Web-based MongoDB admin interface written with Node.js, Express and Bootstrap3.

it can be accessed through <http://swarm-ip:8081>, <http://localhost:8081>, or <http://host-ip:8081> (as appropriate).

## Screenshots

| Home Page                                                      | Database View                                                                  | Collection View                                                     | Editing A Document                                   |
| -------------------------------------------------------------- | ------------------------------------------------------------------------------ | ------------------------------------------------------------------- | ---------------------------------------------------- |
| ![Home Page showing databases](http://i.imgur.com/XiYhblA.png) | ![Viewing collections & buckets in a database](http://i.imgur.com/XWcIgY1.png) | ![Viewing documents in a collection](https://imgur.com/UmGSr3x.png) | ![Editing a document](https://imgur.com/lL38abn.png) |

## Structures

Every folder contains the Dockerfile that will be used by the Docker Compose to build the container.

the other folders and files are necessary for:

**data** -> mongodb folder (shared with Mongo's Container)

**docker-compose-yml** -> is the orchestrator that starts building the containers and link them up.

**WARNING (Windows)**: The default Docker setup on Windows uses a VirtualBox VM to host the Docker daemon, so you cannot use volumes to save the MongoDB data.
