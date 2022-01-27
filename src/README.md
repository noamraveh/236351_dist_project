# Distributed Systems 236351 - Final Project


## Running Instructions


Run the following command from the main directory 

   ```sh
   docker-compose --project-directory ./src -f ./src/docker/docker-compose.yml up
   ```

## About the code


The src folder contains all the necessary code for building and running the project.

### Protos
The proto file defining the various messages and services used for grpc communication between the server

### Server
Contains all the code for the system
    **grpc_client directory**
    Contains the code for the communication between two different grpc clients (sending requests to and from the relevant servers).
    **grpc_server directory**
    Main code for requests - identifying and transferring requests to relevant servers and handling the requests.
    **Server**
    Code for the RESTful APIs used by clients to submit requests.

### etc
Notebook file (.ipynb) for testing and demonstrating the system.
Submits multiple requests for sending coins, submitting transactions (regular and atomic list) and getting ledger history and UTxOs.
