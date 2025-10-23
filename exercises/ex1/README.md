# Exercise 1 - Test the Action Project

## ⚙️ Understand the Action Project

**SAP Build Action** — a low-code/no-code API layer that enables **Joule Skills** to securely interact with any backend system.  
It allows you to define, test, and expose actions without writing complex integration code, making it easier to connect Joule to enterprise data and processes.

In this hands-on scenario, we will use two action projects to connect to an **SAP Business Networks GTT system**. One Action projects  to read Shipment details using its Tracking ID or Delay Status (GTTReadService) & the other to create a shipment (GTTShipment).

The GTTReadService Action project is **already used by two Joule Skills**:
- `Track Shipment`: A Skill to track shipments using its Tracking ID.  
- `Delayed Shipment`: A skill to get all delayed shipments using its Delay Status.

The GTTShipment Action project is used by the Joule Skill: 
- `Create Shipment`: A skill to create shipment or update shipment with ONLY carrier name.

<br>

Now that we understand the Action project’s role in the architecture, let’s test it to confirm that the backend connection works as expected.

## 🧩  Test Action Project

Testing validates that:
- The backend destination (`gttGetService`) is correctly configured and reachable.  
- The action correctly receives and processes input parameters.  
- The output data is as expected.
  
###  Step 1: Open Action Project

In the left panel of the lobby area, expand ‘Connectors’ and click on ‘Actions’

Search for the action project, `GTTReadService`. Click on it to open

<img width="1780" height="424" alt="image" src="https://github.com/user-attachments/assets/e3ea2c66-6da5-45a8-b07a-b0b91141b3eb" />
<br>

<img width="1797" height="517" alt="image" src="https://github.com/user-attachments/assets/9973859d-a4a7-41b7-8e84-7e958033edf0" />


###  Step 2:  Set Required Values for Testing
1. Click on the Test tab.
2. Select the destination as `gttGetService` from the dropdown.
3. enter the requestId filter string as `trackingId eq  '6100005200'`.
4. Click the Test button. 
<img width="1800" height="702" alt="image" src="https://github.com/user-attachments/assets/58225265-f295-4a8e-ad1a-0db5ad8966e3" />

<br><img width="940" height="405" alt="image" src="https://github.com/user-attachments/assets/97668dfc-678d-44c9-ad5e-feacee11c305" />



####  Step 2.1: Provide Values for Input Parameters

Provide the following values for **input parameters** (N1 on the screenshot):
 
| **Parameter** | **Value** | **Description** |
|----------------|------------|-----------------|
| **warehouse** | `TSEB` | Identifies the warehouse where the workload simulation takes place. In this case, `TSEB` represents the warehouse code. |
| **is_simulation** | `true` | Indicates whether the process should run in simulation mode (`true`) or in execution mode (`false`). When set to `true`, no actual assignments or updates are made in the backend — only simulated results are returned. |
| **planning_start** | `2025-10-15T00:00:00Z` | Defines the starting date and time of the planning period for workload and resource distribution analysis. |
| **planning_horizon_to** | `2025-10-16T00:00:00Z` | Specifies the end date and time of the planning horizon — the point until which workload data and assignments are considered. |
| **planning_horizon_from** | `2025-10-15T00:00:00Z` | Marks the lower boundary of the planning horizon, defining from when to begin evaluating workload and resource data. |

####  Step 2.2: Choose the Destination 

On the **righ-top panel** (N2 on the screenshot), select the **destination** associated with the action project:
 | Destination  |
----------|
| `zewm_autonomous-warehouse-agent-srv-api` |

###  Step 3:  Get Succesful API Response 
<br><img width="940" height="471" alt="image" src="https://github.com/user-attachments/assets/fefe3469-cd5d-4923-b5eb-6c274a9afcd4" />
<br> <br> Result: Response should be ‘200 OK’

## 🌟 What's Next

By testing the Action project, we explored the different **input parameters** required for it to function correctly and confirmed that the connection and logic work as expected. 

However, before we start creating the Joule Skill, we first need to **set up a Private Environment for testing**.  
This environment will provide a secure and isolated space to deploy and test the Joule Agents without affecting other configurations.  

Once the Private Environment is ready, we’ll proceed to **use the tested Action** as part of our Joule Skill to complete the end-to-end flow.  

➡️ [**Next Exercise → Exercise 2 – Create a Private Environment for Testing**](https://github.com/SAP-samples/teched2025-AD169/blob/main/exercises/ex2/README.md)

