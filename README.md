> [!IMPORTANT]
> **Welcome to the Agent Builder Lab Preview!**
>
> You are working with a **pre-release version** of the Agent Builder in Joule Studio. This gives you an early look at our upcoming capabilities. Please keep the following in mind:
>
> *   **Features Are Subject to Change:** The user interface (UI), terminology, and functionalities you see in this lab may differ from the final, generally available (GA) product.
> *   **For Educational Use Only:** This environment is designed for learning and experimentation, not for production use.
> *   **Potential Instability:** As a preview version, you may encounter occasional instability or minor bugs. The exercises are designed to work with the current state of the platform. If you get stuck, please notify a session instructor.

# AD-169 - Extend Your Enterprise: Connect Custom AI Agents to Any System

## Description

This exercise shows how to build a simple custom Joule Agent in Joule Studio that uses multiple Joule Skills to solve a warehouse operations task. The agent checks for critical activity areas (by workload) and, if any are critical, runs a simulation to suggest an optimal resource reallocation plan without changing the live system. The agent does basic multi-step reasoning, combines deterministic skills with light calculations, and returns a clear summary for the supervisor.Overview  

## Overview

### Busiess problem and persona   

Before diving into the use case, let's take a moment to get acquainted with our business user from the field who we'll be assisting today. It's really important to understand the business user as thoroughly as possible before building your custom Joule Agent. 

Meet Anna, a Warehouse Operations Supervisor who manages service levels by balancing workload and staff across activities. She requires real-time and forecasted views of workload and staffing by qualifications and time slot, plus safe “what‑if” simulations for reallocating resources without affecting live operations.   


#### Persona — Warehouse Operations Supervisor
![Persona — Warehouse Operations Supervisor](./images/Persona%20—%20Warehouse%20Operations%20Supervisor.jpeg)

#### Pain Points — Warehouse Operations Supervisor
![Pain Points — Warehouse Operations Supervisor](./images/Pain%20Points%20—%20Warehouse%20Operations%20Supervisor.jpeg)

### You will buid a goal-driven Joule Agent in Joule Studio that: 

- Understands a natural-language request on the  warehouse operations 
- Detects overloaded activity areas in warehouses. 
- If critical areas exist, fetch current staffing to run a non-destructive optimization to simulate the best reallocation. 
- Produces a concise, auditable summary for the supervisor. 
- Empoweres Anna in her daily activities  

#### Agent for Warehouse Operations
![Agent for Warehouse Operations](./images/Agent%20for%20Warehouse%20Operations.jpeg)


## Requirements & Prerequisites - already in place

1. Joule Studio in SAP Build 
    - Joule Studio with Agent Builder is enabled and accessible. 

2. CAP application on SAP BTP (middleware to SAP S/4HANA) 
    - Deployed CAP service 
    - BTP Destination configured to reach CAP service 
    - SAP Build Action created to call the CAP endpoint. 
    - Joule Skills “Check Workload Situation” that retrieves a list of activity area workloads created  and “Assign Single Resourceе to Activity Area” were created  
 
3. SAP AI Core for document grounding 

    - Resource group created and assigned.
    - Document grounding pipeline set up and running.
      
## Exercises

<br> Below are the exercises. Please follow them in order to begin your hands-on session
- [Exercise 0 - Getting Started - Login to the Tenant](exercises/ex0/README.md) 
- [Exercise 1 - Test the Action Project](exercises/ex1/README.md) 
- [Exercise 2 - Create a Private Environment for Testing](exercises/ex2/README.md)
- [Exercise 3 - Copy the Project ‘WarehouseOperationsManagement’](exercises/ex3/README.md)
- [Exercise 4 - Create a Joule Skill](exercises/ex4/README.md)
    - [Exercise 4.1 - Define Joule Skill & Input Parameters](exercises/ex4/ex4.1/README.md)
    - [Exercise 4.2 - Bring the SAP Build Action into the Joule Skill & Map Inputs](exercises/ex4/ex4.2/README.md)
    - [Exercise 4.3 - Add a Send message](exercises/ex4/ex4.3/README.md)
    - [Exercise 4.4 - Configure the Output Parameter](exercises/ex4/ex4.4/README.md)

- [Exercise 5 - Create a Joule Agent](exercises/ex5/)
- [Exercise 6 - Test your Joule Agent in Private Environment
](exercises/ex6/)
- [Exercise 7 -Additional Section: Release, Deploy, and Test the Project in a Shared Environment](exercises/ex7/)





## How to obtain support

Support for the content in this repository is available during the actual time of the on-site session for which this content has been designed.

## License
Copyright (c) 2025 SAP SE or an SAP affiliate company. All rights reserved. This project is licensed under the Apache Software License, version 2.0 except as noted otherwise in the [LICENSE](LICENSES/Apache-2.0.txt) file.

## REUSE
[![REUSE status](https://api.reuse.software/badge/github.com/SAP-samples/teched2025-AD169)](https://api.reuse.software/info/github.com/SAP-samples/teched2025-AD169)
