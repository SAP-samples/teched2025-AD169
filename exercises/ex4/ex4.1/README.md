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

> In essence, this Joule Skill transforms slow, manual “what-if” analysis into an **automated, conversational simulation**, improving agility, transparency, and service-level reliability.

---

### 1. Create a New Joule Skill

1. **Click** on the **Create** button and choose **Joule Skill**.  

   <img width="939" height="256" alt="image" src="https://github.com/user-attachments/assets/cbe1290d-5927-46fc-bde3-ad9837c5eb20" />

2. **Enter the Name and Description:**  
   - **Name:** `SimulateWorkforceOptimization`  
   - **Description:** `Simulate Picking Workforce Optimization`

3. **Click** on **Create** to confirm.  

   <img width="939" height="346" alt="image" src="https://github.com/user-attachments/assets/98a9cbea-a8c7-4f93-bf20-5abf982de7b0" />

> 💡 **Good to know:**  
   > Joule and Joule Agents rely on the **Skill Description** to determine **when and how to use** a specific skill.  
   > The description helps the system verify the skill’s intent, understand its context, and match it accurately to the user’s request.  
   > A precise, well-structured description ensures that the right skill is triggered at the right time — improving both **relevance** and **reliability** of the agent’s responses.

---

### 2. Define Skill Inputs and Outputs

4. Once the Joule Skill is created, **click on it** to open the **Skill Builder**.

5. **Click** on the **`<<`** button on the right side of the screen to open the skill’s **Input** and **Output Parameters**.  

   <img width="940" height="291" alt="image" src="https://github.com/user-attachments/assets/c63337c3-a533-4700-b1d0-a8db7c061a1e" />

6. Go to the **Parameters** tab → expand **Skill Inputs** → **click Configure** to define the skill inputs.  

   <img width="940" height="388" alt="image" src="https://github.com/user-attachments/assets/8f6aa26c-46a3-4cd9-a87d-31dcb0ae9766" />

7. **Add the following Inputs with Descriptions.**

   > 💡 **Good to know:**  
   > These inputs correspond directly to the parameters you tested earlier in [Exercise 1 – Test the Action Project](https://github.com/SAP-samples/teched2025-AD169/blob/main/exercises/ex1/README.md).  
   > The Joule Skill will later invoke the same **SAP Build Action** (`WarehouseWorkloadDetermination`) that you validated previously.  
   > This ensures consistency between your Action Project and the Joule Skill, so the data you send and receive aligns seamlessly across both.

   | Serial Number | Name           | Description                                      | Required |
   |----------------|----------------|--------------------------------------------------|-----------|
   | 1 | IsSimulation | Flag to check the simulation | ✅ Checked |
   | 2 | PlanningStart | Planning start date and time converted to UTC | ✅ Checked |
   | 3 | PlanningFrom | Planning from date and time converted to UTC | ✅ Checked |
   | 4 | PlanningTo | Planning to date and time converted to UTC | ✅ Checked |
   | 5 | Warehouse | Warehouse ID | ✅ Checked |


   > [!NOTE]  
   > All **Identifiers** are generated automatically and match the **Name** field.

8. Once all inputs are added, **click Save** to confirm the configuration.

---

✅ **Result:**  
You have successfully created the **Simulate Picking Workforce Optimization** Joule Skill, defining its purpose and input parameters.  

---

➡️ **Next Exercise:** [Exercise 4.2 – Bring the SAP Build Action into the Joule Skill and Map Inputs](https://github.com/SAP-samples/teched2025-AD169/blob/main/exercises/ex4/ex4.2/README.md)
