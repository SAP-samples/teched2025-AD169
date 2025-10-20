# Exercise 1 - Test the Action Project

## ⚙️ Step 1 Understand the Action Project

The **Action project** is an **SAP Build Action** — a low-code/no-code API layer that enables **Joule Skills** to securely interact with any backend system.  
It allows you to define, test, and expose actions without writing complex integration code, making it easier to connect Joule to enterprise data and processes.

In this hands-on scenario, the Action project connects to a **CAP (Cloud Application Programming) application** deployed on **SAP Business Technology Platform (BTP)**. This CAP service acts as middleware between an end user and SAP S/4HANA, managing the communication through predefined endpoints.

This Action project is **already used by two Joule Skills**:
- `Check Workload Situation`: retrieves a list of activity area workloads.  
- `Assign Single Resource to Activity Area`: assigns a selected resource to a specific activity area.  

In this hands-on, we will focus on the 3d Joule Skill — `Simulate Workforce Optimization`,
which reuses the same already created Action project to simulate and optimize workforce distribution across activity areas based on workload and planning horizons.

<br>

Now that we understand the Action project’s role in the architecture, let’s test it to confirm that the backend connection and logic work as expected.

## 🧩 Step 2 Test Action Project

Testing validates that:
- The backend destination (`zewm_autonomous-warehouse-agent-srv-api`) is correctly configured and reachable.  
- The action correctly receives and processes input parameters.  
- The output data and logic behave as designed (for example, `is_simulation = true` triggers a simulation scenario).  

###  Step 2.1: Open Action Project

In the left panel of the lobby area, expand ‘Connectors’ and click on ‘Actions’

Search for the action project, ‘WarehouseWorkloadDetermination’. Click on it to open

<br> <img width="940" height="374" alt="image" src="https://github.com/user-attachments/assets/ab1723c9-cc76-4cd0-8927-30a36ce27b3c" />

###  Step 2.2:  Set Required Values for Testing

<br><img width="940" height="405" alt="image" src="https://github.com/user-attachments/assets/97668dfc-678d-44c9-ad5e-feacee11c305" />

<br> To test the action, provide the following **input parameters** (N1 on the screenshot):

| **Parameter** | **Value** |
|----------------|-----------|
| warehouse | `TSEB` |
| is_simulation | `true` |
| planning_start | `2025-10-15T00:00:00Z` |
| planning_horizon_to | `2025-10-16T00:00:00Z` |
| planning_horizon_from | `2025-10-15T00:00:00Z` |

On the **right side (top panel)**, select the **destination** associated with the action project (N2 on the screenshot):
| **Parameter** |  |
|----------------|-----------|
| **destination** | `zewm_autonomous-warehouse-agent-srv-api` |

###  Step 2.3:  Get Succesful API Response 

<br> <br> Result: Response should be ‘200 OK’
<br><img width="940" height="471" alt="image" src="https://github.com/user-attachments/assets/fefe3469-cd5d-4923-b5eb-6c274a9afcd4" />

<br>Let us use this Action in the next section of the exercise while creating the Joule Skill
<br> <br>  - [Next Exercise - > Exercise 2 - Create a Private Environment for Testing](https://github.com/SAP-samples/teched2025-AD169/tree/6d4d185a4dc5c192ce2f65d6a286b84d98ff7772/exercises/ex2/README.md)
