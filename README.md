# System-Engineering-App
By launching this application you will have an environment that contains mysql database attached to data container and nginx server on top of that there is a simple java springboot application that echo "Welcome To System Engineering Team" on the browser using nginx and the application connected to mysql database.

# Part 1: Docker

## Getting Started
These instructions will get you a copy of the project up and running on your local machine for 

## Prerequisites
Docker-Composer needs to be installed on your local machine

## Installing
1) Browse to http://localhost:8123/
2) Error "This site can’t be reached" should be seen.
3) Run git clone https://github.com/ayasalahbakr/system-engineering.git
4) cd to the project root and run docker-compose up
5) Browse again to http://localhost:8123/

You should see "Welcome To System Engineering Team"

## Built With
1) Java Springboot Platform for running the application
2) Docker-Composer to build the environment (application + MySql + Data Conatiner + Nginx)
3) Some shell commands to generate ssl self signed certificate and dhparam key
    * For generating ssl certificate:
        - openssl req -x509 -sha256 -nodes -newkey rsa:2048 -days 365 -keyout localhost.key -out    localhost.crt
    * For generating dhparam key:
        - openssl req -x509 -sha256 -nodes -newkey rsa:2048 -days 365 -keyout localhost.key -out localhost.crt
        - openssl dhparam -out dhparam.pem 1024


# Part 2: Automation

As the organisation uses Slack for internal communication, the first thing should come to our minds how to integrate and display the status and logs (if possible) of CloudFormation stacks on the team channel , the below diagram will explain an approach how we can do this

<img width="1365" alt="Screen Shot 2019-06-27 at 11 37 11 PM" src="https://user-images.githubusercontent.com/28259567/60302618-8fb71400-9934-11e9-93f4-84e14f3f81ab.png">
