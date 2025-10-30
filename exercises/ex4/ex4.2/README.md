## Exercise 4.2 – Bring the SAP Build Action into the Joule Skill & Map Inputs

In this step, you will connect the **SAP Build Action** tested in [Exercise 1 – Test the Action Project](https://github.com/SAP-samples/teched2025-AD169/blob/main/exercises/ex1/README.md) to your **Joule Skill**, and then map the skill inputs to the action parameters.  
This ensures that when the Joule Agent triggers the skill, it correctly sends and processes all input values through the backend system.

---

### 1. Connect the SAP Build Action

1. In the **Skill Builder**, click on the **+** button to add a new action.  

   <img width="1689" height="472" alt="image" src="https://github.com/user-attachments/assets/1cc46760-2210-4827-9c2f-64492ebc02b8" />


2. From the available options, select **Call Action**

   <img width="1694" height="774" alt="image" src="https://github.com/user-attachments/assets/9e985e2b-8d5f-4797-b997-4f2119cdad00" />


3. From the list of actions displayed, choose the previously tested **SAP Build Action**:  
   - **Action name:** `Invokes action optimizeWorkload`  
   - **Project name:** `WarehouseWorkloadDetermination`

   <img width="658" height="533" alt="image" src="https://github.com/user-attachments/assets/72a3b164-d88d-452b-95c5-c94e25d0e13d" />


   > 💡 **Good to know:**  
   > This step connects your **Joule Skill** with the **SAP Build Action** that encapsulates the business logic you validated earlier.  
   > By linking them, you enable Joule to execute the same backend process through natural language — no manual API calls needed.

4. Once the action call is added, **click on it** to open the right-hand configuration panel for **Input** and **Output Parameters** 

   <img width="1696" height="836" alt="image" src="https://github.com/user-attachments/assets/2b716747-b432-4dd0-9af2-a4d8015deafe" />


5. Add the **Destination Variable** — it defines where the action’s response data will be stored
   - **Destination variable name:** `WHSOPMNG_DEST`

   <img width="1693" height="836" alt="image" src="https://github.com/user-attachments/assets/8bd2a1e3-4bd3-4e54-a30e-c1ab0f75b649" />


   > 💡 **Good to know:**  
   > In this exercise, the **Destination Variable** `WHSOPMNG_DEST` connects the Joule Skill to the backend API destination on your SAP BTP account and captures the results of the `optimizeWorkload` Action.

6. Once you’ve linked the action and destination variable, **click Save** to complete the setup
   <img width="1691" height="839" alt="image" src="https://github.com/user-attachments/assets/d244ad96-8a3a-4827-b562-830c4523a400" />


---

### 2. Map Joule Skill Inputs to Action Parameters

Now you’ll map the **Joule Skill Inputs** (created in [Exercise 4.1](https://github.com/SAP-samples/teched2025-AD169/blob/main/exercises/ex4/ex4.1/README.md)) to the corresponding **Action Inputs** from the SAP Build Action.

1. **Click** on the **Inputs** tab to start mapping the skill inputs to the action call inputs.  
   Select the field `planning_horizon_from`.  

   Since the **Skill Inputs** are of type *String* and some **Action Inputs** are of type *DateTime*, click **Apply a formula** to perform the mapping.  

   <img width="939" height="465" alt="image" src="https://github.com/user-attachments/assets/4fdea1c3-f6b7-437b-8ebe-25a31a107552" />

   <img width="940" height="368" alt="image" src="https://github.com/user-attachments/assets/22cbc3bb-e60d-4d51-97d3-7262078e5482" />

2. In the **Formula Editor**, type `PlanningFrom`.  
   Then click **Apply**.  

   <img width="940" height="386" alt="image" src="https://github.com/user-attachments/assets/01426f05-ccfc-462a-8a9e-674f658b10fe" />  

   <img width="940" height="541" alt="image" src="https://github.com/user-attachments/assets/015e3fcd-d755-40a8-933d-6fc89a1ab869" />

3. Similarly, map the following fields:

   | **Action Inputs** | **Skill Content / Skill Input Variables** |
   |--------------------|-------------------------------------------|
   | `planning_horizon_to` | `PlanningTo` |
   | `planning_start` | `PlanningStart` |

4. Next, click on the field `is_simulation` and select **Apply a formula**.  
   In the **Functions** section, expand **Boolean functions** and choose **ValuesAreEqual**.  
   Then click **Insert**.  

   <img width="940" height="466" alt="image" src="https://github.com/user-attachments/assets/0af0a409-99a9-4443-893e-61cd2615e6e6" />

   Add the values in the brackets as `("true", "true")`, and click **Apply**.  

   <img width="940" height="509" alt="image" src="https://github.com/user-attachments/assets/bfd812f5-6a73-4bea-b1ae-bd3e1759a5d2" />

5. Map the variable `Warehouse` with the skill input `Warehouse`.  

   <img width="939" height="418" alt="image" src="https://github.com/user-attachments/assets/55821163-09bd-434b-b91f-c5f35842bdc9" />

6. Once all mappings are completed, click **Save** to store the configuration.

---

✅ **Result:**  
You have successfully connected your **Joule Skill** to the **SAP Build Action** and mapped all input variables.  
When the Joule Agent executes this skill, it will automatically send the mapped input values to the backend API destination and receive the optimized workload simulation results.

---

➡️ **Next Exercise:** [Exercise 4.3 – Add a Send Message in Joule Skill](https://github.com/SAP-samples/teched2025-AD169/blob/main/exercises/ex4/ex4.3/README.md)
