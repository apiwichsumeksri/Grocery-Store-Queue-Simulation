🛒 Grocery Store Queue Simulation (C++)
Overview

This project is a C++ grocery store queue simulation developed as part of the ECE 244 – Programming Fundamentals course.
The program models customer flow through checkout registers using either:

Single shared queue, or

Multiple independent queues (one per register)

The simulation processes time-based events such as customer arrivals, register openings/closings, and customer departures, and reports wait-time statistics at the end.

Features

Event-driven simulation using command input

Supports single-queue and multiple-queue modes

Dynamic register management (open / close at runtime)

Linked-list–based queue implementation

Tracks:

Maximum wait time

Average wait time

Standard deviation of wait time

Explicit dynamic memory management (no leaks)

File Structure
.
├── main.cpp              # Simulation driver and command handling
├── Customer.h / .cpp     # Customer object (arrival, departure, items)
├── QueueList.h / .cpp    # Linked-list queue implementation
├── Register.h / .cpp     # Register logic and timing
├── RegisterList.h / .cpp # List of active registers
└── README.md

How It Works

User selects single or multiple queue mode at startup

Commands are read from standard input:

Open a register

Close a register

Add a customer

The simulation advances time incrementally

Customers are served based on register availability and queue rules

At program termination, wait-time statistics are printed

Example Commands
register open 1 2.0 5.0 3.0
customer 10 1.5
customer 5 2.0
register close 1 4.0

Compilation & Execution
g++ -std=c++11 *.cpp -o grocery_sim
./grocery_sim

Academic Integrity Notice

⚠️ Important

This repository is published for learning, demonstration, and portfolio purposes only.

Do not copy or submit this code for coursework.

Students currently enrolled in ECE 244 (or similar courses) should use this repository only as a conceptual reference.

The implementation reflects my own understanding and design decisions, written independently.

Skills Demonstrated

C++ object-oriented design

Linked lists and dynamic memory management

Event-driven simulation logic

Clean separation of concerns

Defensive input handling
