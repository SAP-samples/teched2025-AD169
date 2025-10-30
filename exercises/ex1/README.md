# Exercise 1 - Test the Action Project

## ⚙️ Understand the Action Project

**SAP Build Action** — a low-code/no-code API layer that enables **Joule Skills** to securely interact with any backend system.  
It allows you to define, test, and expose actions without writing complex integration code, making it easier to connect Joule to enterprise data and processes.

In this hands-on scenario, the Action project connects to a **CAP (Cloud Application Programming) application** deployed on **SAP Business Technology Platform (BTP)**. This CAP service acts as middleware between an end user and SAP S/4HANA, managing the communication through predefined endpoints.

This Action project is **already used by two Joule Skills**:
- `Check Workload Situation`: retrieves a list of activity area workloads.  
- `Assign Single Resource to Activity Area`: assigns a selected resource to a specific activity area.  

In this hands-on, we will focus on the 3d Joule Skill — `Simulate Workforce Optimization`,
which reuses the same already created Action project to simulate and optimize workforce distribution across activity areas based on workload and planning horizons.

<br>

Now that we understand the Action project’s role in the architecture, let’s test it to confirm that the backend connection and logic work as expected.



## 🧩  Test Action Project

Testing validates that:
- The backend destination (`zewm_autonomous-warehouse-agent-srv-api`) is correctly configured and reachable.  
- The action correctly receives and processes input parameters.  
- The output data and logic behave as designed (for example, `is_simulation = true` triggers a simulation scenario).  



###  Step 1: Open Action Project

In the left panel of the lobby area, expand ‘Connectors’ and click on ‘Actions’


<img width="1700" height="833" alt="image" src="https://github.com/user-attachments/assets/cb67767f-20a2-4c76-9b0b-d99b1c3eff10" />


Search for the action project, ‘WarehouseWorkloadDetermination’. Click on it to open

<img width="1689" height="799" alt="image" src="https://github.com/user-attachments/assets/4a1c6092-771f-4fac-8857-17674d28b846" />




###  Step 2:  Set Required Values for Testing

Click the 'Test' Tab

<img width="1700" height="838" alt="image" src="https://github.com/user-attachments/assets/42f0917f-8dba-43d8-9281-5a3f41e66f97" />


Here we see the categories 'Connectivity' and the 'Test Input Values'

<img width="1686" height="841" alt="image" src="https://github.com/user-attachments/assets/5b956f9a-90b0-4c1f-9cf6-57e9760d2b06" />




####  Step 2.1: Choose the Destination 

On the **righ-top panel** (N2 on the screenshot), select the **destination** associated with the action project:
 | Destination  |
----------|
| `zewm_autonomous-warehouse-agent-srv-api` |

<img width="1695" height="892" alt="image" src="https://github.com/user-attachments/assets/de175383-c27b-41c2-8489-8255d80a818e" />



####  Step 2.2: Provide Values for Input Parameters

Provide the following values for **input parameters** (N1 on the screenshot):
 
| **Parameter** | **Value** | **Description** |
|----------------|------------|-----------------|
| **warehouse** | `TSEB` | Identifies the warehouse where the workload simulation takes place. In this case, `TSEB` represents the warehouse code. |
| **is_simulation** | `true` | Indicates whether the process should run in simulation mode (`true`) or in execution mode (`false`). When set to `true`, no actual assignments or updates are made in the backend — only simulated results are returned. |
| **planning_start** | `2025-10-15T00:00:00Z` | Defines the starting date and time of the planning period for workload and resource distribution analysis. |
| **planning_horizon_to** | `2025-10-16T00:00:00Z` | Specifies the end date and time of the planning horizon — the point until which workload data and assignments are considered. |
| **planning_horizon_from** | `2025-10-15T00:00:00Z` | Marks the lower boundary of the planning horizon, defining from when to begin evaluating workload and resource data. |

<img width="1698" height="854" alt="image" src="https://github.com/user-attachments/assets/f8d35279-075d-4017-9e24-455ec3b1a3c3" />



###  Step 3:  Get Succesful API Response 

To the **right** of your screen, select the **Test Button**

<img width="1695" height="895" alt="image" src="https://github.com/user-attachments/assets/12b11c3b-db14-445e-9623-30e96bfc0294" />

###  Step 4:  Check the Test Result Response to be in green and ‘200 OK’

<img width="1703" height="897" alt="image" src="https://github.com/user-attachments/assets/5fd5dc05-dab1-4f53-bf37-005d9a80301b" />


## 🌟 What's Next

By testing the Action project, we explored the different **input parameters** required for it to function correctly and confirmed that the connection and logic work as expected. 

However, before we start creating the Joule Skill, we first need to **set up a Private Environment for testing**.  
This environment will provide a secure and isolated space to deploy and test the Joule Agents without affecting other configurations.  

Once the Private Environment is ready, we’ll proceed to **use the tested Action** as part of our Joule Skill to complete the end-to-end flow.  

➡️ [**Next Exercise → Exercise 2 – Create a Private Environment for Testing**](https://github.com/SAP-samples/teched2025-AD169/blob/main/exercises/ex2/README.md)
