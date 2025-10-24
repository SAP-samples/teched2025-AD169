## Exercise 4.1 –  Define Joule Skill with Input & Output Parameters

1. **Click** on the **Create** button and choose **Joule Skill**.  

   <img width="939" height="256" alt="image" src="https://github.com/user-attachments/assets/cbe1290d-5927-46fc-bde3-ad9837c5eb20" />

2. **Enter the Name and Description:**  
   - **Name:** `SimulateWorkforceOptimization`  
   - **Description:** `Simulate Picking Workforce Optimization`

<br> 

   > 💡 **Good to know:**
   >  
   > Joule and Joule Agents rely on the **Skill Description** to determine **when and how to use** a specific skill.  
   > The description helps the system verify the skill’s intent, understand its context, and match it accurately to the user’s request.  
   > A precise, well-structured description ensures that the right skill is triggered at the right time — improving both **relevance** and **reliability** of the agent’s responses.

<br>

**Click** on the **Create**  to confirm.  

   <img width="939" height="346" alt="image" src="https://github.com/user-attachments/assets/98a9cbea-a8c7-4f93-bf20-5abf982de7b0" />

3. Once the Joule Skill is created, **click on it** to open the **Skill Builder**.

4. **Click** on the **`<<`** button on the right side of the screen to open the skill’s **Input** and **Output Parameters**.  

   <img width="940" height="291" alt="image" src="https://github.com/user-attachments/assets/c63337c3-a533-4700-b1d0-a8db7c061a1e" />

5. Go to the **Parameters** tab → expand **Skill Inputs** → **click** **Configure** to define the skill inputs.  

   <img width="940" height="388" alt="image" src="https://github.com/user-attachments/assets/8f6aa26c-46a3-4cd9-a87d-31dcb0ae9766" />



6. **Add the following Inputs with Descriptions.**

   > 💡 **Good to know:**  
   > These inputs correspond directly to the parameters you tested earlier in [Exercise 1 – Test the Action Project](https://github.com/SAP-samples/teched2025-AD169/blob/main/exercises/ex1/README.md).  
   > The Joule Skill will invoke the same **SAP Build Action** (`WarehouseWorkloadDetermination`) that you validated previously.  
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

   Once all inputs are added, **Click** on the **Create**  **Save**.

---

➡️ **Next Exercise:** [Exercise 4.2 – Mapping Input Variables of the Action Project with Joule Skill Inputs](https://github.com/SAP-samples/teched2025-AD169/blob/main/exercises/ex4/ex4.2/README.md)
