# Matchmaking Office System

This repository contains a C++ program designed to simulate a matchmaking office. The system manages a database of clients, facilitates matchmaking based on specific criteria, and provides functionalities for adding, removing, and querying clients.

## Overview

The program demonstrates object-oriented programming principles in C++ by implementing classes to handle strings, clients, matchmaking agency operations, and menu management. The system supports functionalities for managing client information, performing matches, and interacting with the user.

## Classes and Functionalities

### 1. String Class

- **Fields**:
  - `char*` (pointer to a dynamically allocated string)

- **Methods**:
  - **Constructor**: Initializes the string, removing unnecessary spaces.
  - **Copy Constructor**: Performs a deep copy of the string.
  - **Destructor**: Frees dynamically allocated memory.
  - **Assignment Operator `=`**: Performs a deep copy of the string.
  - **Comparison Operator `==`**: Compares the content of two strings.
  - **Output Operator `<<`**: Prints the string to the output stream.

### 2. Client Class

- **Fields**:
  - `String` (ID number of the client)
  - `String` (full name of the client)
  - `char` (gender of the client: 'M' or 'F')
  - `double` (age of the client, must be at least 18)
  - `int` (number of hobbies)
  - `char*` (list of hobbies, dynamically allocated)

- **Methods**:
  - **Constructor**: Initializes all fields, performing a deep copy of the string and hobbies.
  - **Copy Constructor**: Performs a deep copy of the client object.
  - **Destructor**: Frees dynamically allocated memory for hobbies.
  - **Assignment Operator `=`**: Performs a deep copy of the client object.
  - **Comparison Operator `==`**: Compares two clients based on gender, age difference, and common hobbies.

### 3. MatchMakingAgency Class

- **Fields**:
  - `int` (number of clients in the agency)
  - `std::vector<Client>` (dynamic list of clients)

- **Methods**:
  - **Default Constructor**: Initializes an empty database.
  - **Destructor**: Frees dynamically allocated memory.
  - **Assignment Operator `=`**: Performs a deep copy of the agency.
  - **Add Client Operator `+=`**: Adds a client to the list if not already present.
  - **Remove Client Operator `-=`**: Removes a client from the list if present.
  - **Print Matches Method**: Prints all clients matching a given client's criteria.
  - **Output Operator `<<`**: Prints the list of all clients and their details.

### 4. Menu Class

- **Fields**:
  - `MatchMakingAgency` (database of clients)

- **Methods**:
  - **Constructor**: Initializes an empty database.
  - **Display Menu**: Displays a menu with options to add, remove, print clients, or print matches.

## Main Function

The `main` function initializes a `Menu` object and displays the main menu, allowing users to interact with the system.

## Usage

1. **Compile the Program**:
   ```bash
   g++ -o matchmaking_system main.cpp
2. **Run the Program**:
   ```bash
   ./matchmaking_system
3. **Menu Options**:
1) Add a New Client: Enter client details to add a new client to the database.
2) Remove an Existing Client: Enter the client ID to remove an existing client from the database.
3) Print All Clients: Print details of all clients in the database.
4) Print All Matches for a Client: Enter a client ID to print all possible matches.
5) Quit the Program: Exit the program.
