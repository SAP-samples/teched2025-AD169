## Exercise 4.4 – Configure the Output Parameter

In this exercise, you will configure the **Output Parameter** for your Joule Skill.  
This is an important step — the end result defined here will later be used by the **Joule Agent** to interpret and summarize the simulation data.

---

### ⚙️ Why This Matters

The **Output Parameter** determines what data your Joule Skill returns after executing the backend action.  
When the Joule Agent calls this skill, it relies on this structured output to understand the result, verify it, and use it for reasoning or subsequent actions.  
Proper configuration ensures a smooth and accurate flow of data between your **Skill** and the **Agent**.

---

### Step 1: Define the Output Parameter

👉 1.1 In the **Skill Builder**, click on the **End** button

👉 1.2 Click on **Define Skill outputs**

👉 1.3 Then click on **Parameters** tab (right panel), and in the **Outputs Section** click on **Configure**

👉 1.4 Click **Add Output** and **PASTE** these values in each field :

   | Field | Value |
   |--------|--------|
   | **Name** | `WorkloadOptimizationResults` |
   | **Description** | `Workload Optimization Results` |
   | **Type** | `post_postWarehouseWorkloa__viceOptimizeWorkload_200_output_schema`|
   | **Required**| `Ticked`|

👉 1.5 Click **Apply** to confirm

   <img width="940" height="465" alt="image" src="https://github.com/user-attachments/assets/0cebad6a-d14c-457a-837c-d974d6e0752a" />

---

### Step 2: Map the Output Variable

👉 1.1 Click on the **End** button again

👉 1.2 Click on the output field to **Select Item and map the result** from your previous **Action Call** step to the **Output Variable** you just created in the mapping panel 

   <img width="939" height="410" alt="image" src="https://github.com/user-attachments/assets/9a92b8ea-4fd5-41a2-aab0-15deabb4d808" />

---
### Step 3: Map the Output Variable

👉 Click on Save

---

✅ **Result:**  
You have successfully configured the **Output Parameter** for your Joule Skill.  
This ensures the **Joule Agent** can later access and interpret the simulation results correctly when executing the complete scenario.

---

➡️ **Next Exercise:** [Exercise 5 – Creation of an Agent](https://github.com/SAP-samples/teched2025-AD169/blob/main/exercises/ex5/README.md)
