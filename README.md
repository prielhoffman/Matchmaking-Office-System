# Matchmaking Office Management System

A **C++ object-oriented application** for managing a matchmaking office database, including client registration, removal, listing, and compatibility-based match suggestions.

This project demonstrates core **OOP design**, **dynamic memory management**, **operator overloading**, and building an interactive **menu-driven system** in C++.

## Tech Stack

- **Language:** C++
- **Concepts:** object-oriented programming, dynamic memory management, deep copy, operator overloading, vectors, CLI applications

## What the Project Does

The system simulates the workflow of a matchmaking office.

It allows the user to:

- add new clients to the agency database
- remove existing clients
- print the full client list
- find potential matches for a selected client based on predefined compatibility rules

The project focuses on building the system from custom classes and internal logic rather than relying on high-level abstractions. :contentReference[oaicite:1]{index=1}

## Main Features

- client database management
- matchmaking based on compatibility rules
- add / remove / query operations
- object-oriented system design
- custom string handling
- deep-copy semantics
- operator overloading
- interactive menu-driven interface

## System Design

The project is organized around four main classes.

### 1. `String` Class

A custom string class used to manage character data with dynamic memory allocation.

It includes:

- constructor
- copy constructor
- destructor
- assignment operator
- equality comparison
- output operator

This class demonstrates manual memory handling and deep-copy behavior. :contentReference[oaicite:2]{index=2}

### 2. `Client` Class

Represents a client in the matchmaking system.

Each client includes:

- ID number
- full name
- gender
- age
- hobbies

The class supports:
- proper construction and destruction
- copying and assignment
- comparison for matchmaking compatibility

Compatibility is determined using criteria such as gender, age difference, and common hobbies. :contentReference[oaicite:3]{index=3}

### 3. `MatchMakingAgency` Class

Manages the collection of clients in the system.

It is responsible for:

- storing all clients
- adding new clients
- removing clients
- printing the full database
- finding matching clients for a given user

This class acts as the main business-logic layer of the application. :contentReference[oaicite:4]{index=4}

### 4. `Menu` Class

Handles user interaction through a command-line menu.

It provides the interface for:
- adding clients
- removing clients
- printing all clients
- printing matches
- exiting the program

This keeps user interaction separate from the core data and matching logic. :contentReference[oaicite:5]{index=5}

## What I Implemented

This project focused on building a complete C++ system with clean class responsibilities and proper resource management.

Key implementation areas included:

- designing multiple interacting classes
- implementing deep-copy semantics
- managing dynamically allocated memory safely
- overloading operators for cleaner class behavior
- storing and managing a dynamic client database
- implementing compatibility-based matching logic
- building a command-line user interface

## Why This Project Matters

This project demonstrates practical understanding of:

- object-oriented design in C++
- memory management with constructors, destructors, and copy semantics
- operator overloading
- class-based system architecture
- encapsulating business logic in reusable components
- building an interactive CLI application

It is a strong foundational C++ project because it combines data modeling, logic design, and user interaction in one system.

## Matchmaking Logic

The system compares clients based on predefined compatibility rules.

According to the current implementation, the matching logic uses factors such as:

- gender
- age difference
- shared hobbies

This makes the project more than a simple CRUD system — it also includes rule-based comparison logic between entities. :contentReference[oaicite:6]{index=6}

## How to Run

Compile the program:

```bash
g++ -o matchmaking_system main.cpp
```

Run the program:

```bash
./matchmaking_system
```

## Menu Options

The system provides the following menu actions:

1. Add a new client  
2. Remove an existing client  
3. Print all clients  
4. Print all matches for a client  
5. Quit the program :contentReference[oaicite:7]{index=7}

## Core Concepts Practiced

- object-oriented programming
- class design
- dynamic memory allocation
- deep copy
- constructors and destructors
- operator overloading
- vectors
- CLI program design
- rule-based matching logic

## Key Takeaways

Through this project, I strengthened my understanding of:

- how to design a multi-class C++ application
- how to manage dynamically allocated memory safely
- how copy constructors and assignment operators affect object behavior
- how to separate data, business logic, and user interaction
- how to build an interactive console application with structured logic

## Future Improvements

Possible next steps for the project:

- replace the custom string class with `std::string` in a modernized version
- improve input validation and error handling
- support richer compatibility scoring
- persist client data to files or a database
- add unit tests for matching logic
- refactor the CLI into a cleaner command-handling structure
