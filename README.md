# Elevator Simulation Project

## Overview

This project is a **multi-threaded elevator control and simulation system** implemented in **Java**, developed to model how real-world elevators operate within a building. The system simulates **multiple elevators running concurrently**, coordinated by a centralized **scheduler**, and includes a fully functional **graphical user interface (GUI)** for real-time interaction and visualization.

The simulation emphasizes **concurrency, synchronization, state-based behavior, and fault handling**, closely mirroring challenges found in real embedded and distributed control systems.

---

## Core Concepts Demonstrated

* Concurrent programming with **Java threads**
* **Finite State Machines (FSMs)** for elevator and scheduler behavior
* Thread-safe request handling and synchronization
* Real-time system simulation with GUI integration
* Fault modeling and system robustness

---

## System Architecture

### Elevator

* Each `Elevator` runs in its **own thread**, allowing multiple elevators to operate independently and in parallel
* Maintains internal state via the `ElevatorState` enum (e.g., Idle, Moving, DoorsOpen)
* Simulates realistic timing for movement, door operations, and request servicing
* Includes logic for handling **movement and door-related faults**

### Scheduler

* Implemented as a centralized controller responsible for:

  * Receiving floor requests
  * Assigning requests to elevators based on availability and state
  * Coordinating system-wide behavior
* Operates concurrently with elevator threads to simulate real-time dispatching

### Floor System

* Represents building floors and external elevator requests
* Reads requests from input files (e.g., `FloorRequests.txt`) to simulate realistic traffic patterns
* Communicates asynchronously with the scheduler

### Graphical User Interface (GUI)

* Provides a real-time visualization of:

  * Elevator positions
  * Direction of movement
  * Current states and requests
* Allows users to interact with the system and observe how concurrent components respond dynamically

---

## Fault Simulation

The system includes explicit modeling of elevator faults to test robustness and correctness, such as:

* Door operation failures
* Movement-related faults while traveling to a destination

Fault behavior is documented and supported with **UML state machines, timing diagrams, and sequence diagrams**, included in the project documentation.

---

## Technologies Used

* **Language:** Java
* **Concurrency:** Java Threads, synchronization primitives
* **GUI:** Java-based GUI framework
* **Design Artifacts:** UML class diagrams, sequence diagrams, timing diagrams
* **Testing:** Dedicated system-level test classes

---

## Project Structure

```
src/
 ├── Elevator.java
 ├── ElevatorState.java
 ├── Scheduler.java
 ├── Floor.java
 ├── GUI.java
 ├── *Test.java
```

Additional documentation, UML diagrams, and design artifacts are included in the repository root.

---

## Why This Project Is Significant

This project demonstrates the ability to design and implement a **realistic concurrent control system**, addressing challenges such as:

* Coordinating multiple independent threads
* Preventing race conditions and inconsistent states
* Managing asynchronous events and shared resources
* Modeling and recovering from system faults

Elevator systems are a classic example of real-time scheduling and concurrency problems, making this project a strong demonstration of practical software engineering skills.

---

## How to Run

1. Open the project in an IDE such as Eclipse or IntelliJ
2. Build the project using the provided configuration
3. Run the main GUI class
4. Submit elevator requests and observe concurrent system behavior

---
