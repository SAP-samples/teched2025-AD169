## Exercise 4.1 – Define Joule Skill & Input Parameters

In this exercise, you will create a new **Joule Skill** called **Simulate Picking Workforce Optimization**.
This skill forms the foundation of the **Agentic Warehouse Operations** use case, and will enable the AI Agent to simulate and optimize workforce allocation across warehouse activity areas.

---

### ⚙️ **Why We Need This Joule Skill**

The **Simulate Picking Workforce Optimization** Joule Skill will allow the **Warehouse Operations Agent** to perform intelligent, data-driven workload balancing without disrupting live operations.  

By using this Joule Skill, the Agent will be able to:  
- Fetch **real-time workload and staffing data** from backend systems.  
- Run a **non-disruptive optimization simulation** to suggest the best reallocation of resources.  
- Return results that include **staffing recommendations**, **surplus/deficit per area**, and **projected KPI/SLA impact**.  

In essence, this Joule Skill transforms slow, manual “what-if” analysis into an **automated, conversational simulation**, improving agility, transparency, and service-level reliability.

---

### Step 1: Create a New Joule Skill

👉 1.1 **Click** on the **Create** button and choose **Joule Skill**.  

   <img width="1683" height="496" alt="image" src="https://github.com/user-attachments/assets/d9d7b648-1a84-4250-bf3a-8172bebe4930" />


👉 1.2 **Enter the Name and Description:**  
   - **Name:** `SimulateWorkforceOptimization`  
   - **Description:** `Simulate Picking Workforce Optimization`

👉 1.3 **Click** on **Create** to confirm.  

   <img width="648" height="365" alt="image" src="https://github.com/user-attachments/assets/90e30b30-a887-4a07-a049-62b711e27291" />


> 💡 **Good to know:**  
   > Joule and Joule Agents rely on the **Skill Description** to determine **when and how to use** a specific skill.  
   > The description helps the system verify the skill’s intent, understand its context, and match it accurately to the user’s request.  
   > A precise, well-structured description ensures that the right skill is triggered at the right time — improving both **relevance** and **reliability** of the agent’s responses.

---

### Step 2: Define Skill General Parameters

👉 2.1 Once the Joule Skill is created, **click on it** to open the **Skill Builder**.

👉 2.2 **Click** on the **`<<`** button on the right side of the screen to open the skill’s General Parameters
   <img width="1690" height="833" alt="image" src="https://github.com/user-attachments/assets/a4fedbc1-b90a-4abd-90ff-64cd7b86f210" />


👉 2.3 **Disable** the **"Allow skill to be started directly by a user"** Toggle. This will restrict this skill to only be called as a tool from an Agent
   
   <img width="1691" height="836" alt="image" src="https://github.com/user-attachments/assets/3e58cb2d-c6c7-438a-8d08-3a9cd0715c8e" />


### Step 3: Define Skill Inputs and Outputs

👉 3.1 Go to the **Parameters** tab → expand **Skill Inputs** → **click Configure** to define the skill inputs.  

   <img width="1691" height="551" alt="image" src="https://github.com/user-attachments/assets/96588b22-b8b0-490a-98da-7b6b7fd9040a" />


👉 3.2 **Add the following Inputs with Descriptions.**

   | Name           | Description                                      | Type      | Required |
   |----------------|--------------------------------------------------|-----------|-----------|
   | `IsSimulation` | Flag to check the simulation | String | ✅ Checked |
   | `PlanningStart` | Planning start date and time converted to UTC | DateTime | ✅ Checked |
   | `PlanningFrom` | Planning from date and time converted to UTC | DateTime | ✅ Checked |
   | `PlanningTo` | Planning to date and time converted to UTC | DateTime | ✅ Checked |
   | `Warehouse` | Warehouse ID | String | ✅ Checked |

> [!NOTE]  
> All **Identifiers** are generated automatically and match the **Name** field.

<img width="1915" height="782" alt="image" src="https://github.com/user-attachments/assets/e686f489-c999-4869-9bb9-907980a25d2f" />

   These inputs correspond directly to the parameters you tested earlier in [Exercise 1 – Test the Action Project](https://github.com/SAP-samples/teched2025-AD169/blob/main/exercises/ex1/README.md).
   The Joule Skill will later invoke the same **SAP Build Action** (`WarehouseWorkloadDetermination`) that you validated previously.
   This ensures consistency between your Action Project and the Joule Skill, so the data you send and receive aligns seamlessly across both.

> 💡 **Good to know:**  
> The **Input Description** is also important — here you can explain in **natural language** the expected data format for Joule, such as specifying **time**, **dates**, or **identifiers**.  
> This helps Joule and Joule Agents correctly interpret user inputs and improves response accuracy.


👉 3.3 Once all inputs are added, **click Save** to confirm the configuration.

---

✅ **Result:**  
You have successfully created the **Simulate Picking Workforce Optimization** Joule Skill, defining its purpose and input parameters.  

---

➡️ **Next Exercise:** [Exercise 4.2 – Bring the SAP Build Action into the Joule Skill and Map Inputs](https://github.com/SAP-samples/teched2025-AD169/blob/main/exercises/ex4/ex4.2/README.md)
