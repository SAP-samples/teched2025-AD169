# AD-169 - Extend Your Enterprise: Connect Custom AI Agents to Any System

## Description

This exercise shows how to build a simple custom Joule Agent in Joule Studio that uses multiple Joule Skills to solve a warehouse operations task. The agent checks for critical activity areas (by workload) and, if any are critical, runs a simulation to suggest an optimal resource reallocation plan without changing the live system. The agent does basic multi-step reasoning, combines deterministic skills with light calculations, and returns a clear summary for the supervisor.Overview  

## Overview

### Busiess problem and persona   

Before diving into the use case, let's take a moment to get acquainted with our business user from the field who we'll be assisting today. It's really important to understand the business user as thoroughly as possible before considering the Joule Agent. 

Meet Anna, a Warehouse Operations Supervisor who manages service levels by balancing workload and staff across activities. She requires real-time and forecasted views of workload and staffing by qualifications and time slot, plus safe “what‑if” simulations for reallocating resources without affecting live operations.   

### You will buid a goal-driven Joule Agent in Joule Studio that: 

- Understands a natural-language request on the  warehouse operations 
- Detects overloaded activity areas in warehouses. 
- If critical areas exist, fetch current staffing to run a non-destructive optimization to simulate the best reallocation. 
- Produces a concise, auditable summary for the supervisor. 
- Empoweres Anna in her daily activities  




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
- [Exercise 0 - Getting Started - Login to the Tenant](exercises/ex0/) 
- [Exercise 1 - Test the Action Project](exercises/ex1/) 
- [Exercise 2 - Create a Private Environment for Testing](exercises/ex2/)
- [Exercise 3 - Copy the Project ‘WarehouseOperationsManagement’](exercises/ex3/)
- [Exercise 4 -Creation of a new Joule Skill](exercises/ex4/)
    - [Exercise 4.1 - Exercise 4 Sub Exercise 1 Description](exercises/ex4/ex4.1/README.md)
    - [Exercise 4.2 - Exercise 4 Sub Exercise 2 Description](exercises/ex4/ex4.2/README.md)
    - [Exercise 4.3 - Exercise 4 Sub Exercise 3 Description](exercises/ex4/ex4.3/README.md)
    - [Exercise 4.4 - Exercise 4 Sub Exercise 4 Description](exercises/ex4/ex4.4/README.md)
     
- [Exercise 5 -Creation of an Agent](exercises/ex5/)
- [Exercise 6 -Creation of an Agent](exercises/ex6/)
- [Exercise 7 -Additional Section](exercises/ex7/)
    - [Exercise 7.1 - Exercise 7 Sub Exercise 1 Description](exercises/ex7/README.md)
    - [Exercise 7.2 - Exercise 7 Sub Exercise 2 Description](exercises/ex7/README.md)

**OR** Link to the Tutorial Navigator for example...

Start the exercises [here](https://developers.sap.com/tutorials/abap-environment-trial-onboarding.html).

**IMPORTANT**

Your repo must contain the .reuse and LICENSES folder and the License section below. DO NOT REMOVE the section or folders/files. Also, remove all unused template assets(images, folders, etc) from the exercises folder. 

## Contributing
Please read the [CONTRIBUTING.md](./CONTRIBUTING.md) to understand the contribution guidelines.

## Code of Conduct
Please read the [SAP Open Source Code of Conduct](https://github.com/SAP-samples/.github/blob/main/CODE_OF_CONDUCT.md).

## How to obtain support

Support for the content in this repository is available during the actual time of the online session for which this content has been designed. Otherwise, you may request support via the [Issues](../../issues) tab.

## License
Copyright (c) 2024 SAP SE or an SAP affiliate company. All rights reserved. This project is licensed under the Apache Software License, version 2.0 except as noted otherwise in the [LICENSE](LICENSES/Apache-2.0.txt) file.
