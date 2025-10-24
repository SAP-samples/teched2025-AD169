## Exercise 5 – Creation of a Joule Agent

In this exercise, you will create the **Warehouse Workforce Optimization Agent** — an intelligent Joule Agent that analyzes warehouse workloads, detects critical activity areas, and recommends or executes workforce reallocation.  

This agent brings together the Joule Skills you created earlier to enable autonomous, data-driven warehouse management.

---

### ⚙️ Why This Matters

While **Joule Skills** define *what* actions can be performed (e.g., analyze workloads or simulate optimizations), the **Joule Agent** defines *how* these skills are orchestrated in a conversational, goal-driven workflow.  

This agent:
- Combines multiple Joule Skills into an intelligent flow.  
- Makes autonomous decisions based on data and context.  
- Communicates naturally with warehouse supervisors.  

In short, this is where your **Agentic Warehouse Operations** scenario becomes fully functional.

---

### 1. Create a New Joule Agent

1. In the **overview page** of your project, click on the dropdown **Create → Joule Agent**.  

   <img width="940" height="320" alt="image" src="https://github.com/user-attachments/assets/4a2e4dd5-7751-45e4-9cb1-b33d82299321" />

2. Enter the following details:  
   - **Name:** `Warehouse Workforce Optimization Agent`  
   - **Description:** `Agent to check critical workloads in the warehouse and execute optimal reassignment of workforce to activity areas.`  

---

### 2. Configure the Agent Behavior

#### 🧠 Expertise

`> You are responsible for analyzing critical activity areas in terms of workload and, if needed, simulating or optimizing workforce allocation.`

---

#### 🧭 Instructions

> You should always start by analyzing the critical activity areas using the skill **CheckingPickingWorkloadSituation**.  
> Based on the user’s request, determine whether to perform a **simulation** or a **real workforce optimization**.  
> Before performing any action, ensure that all required parameters — **warehouse**, **planning from**, **planning to**, and **planning start datetime** — are provided by the user.  
>  
>  **Pre-requisites**  
> - Verify that all required parameters are provided.  
> - Ensure proper date/time formatting (**UTC**).  
> - Validate the warehouse context before executing optimization.  
>  
>  **Available Skills**  
>  
> **1. Checking Picking Workload Situation**  
> - Verifies the picking workload situation and determines workload per activity area.  
> - Identifies critical areas where workload **> 100**.  
> - Summarizes identified activity areas and their workloads.  
> - If no critical areas exist, stop further actions.  
>  
> **2. Simulate Workforce Optimization**  
> - Simulates optimal workforce allocation using current context parameters.  
> - Summarizes rebalanced and redundant resources.  
> - If no results are returned, stop further actions.  
>  
> **3. Execute Real Workforce Optimization**  
> - Executes real workforce allocation using context parameters.  
> - Summarizes rebalanced and redundant resources.  
> - If no results are returned, stop further actions.  
> - Re-check the workload situation and finalize without additional actions.



#### 💬 Additional Context

> **Things to Note**  
>  
> - The date/time parameters **PlanningFrom**, **PlanningTo**, and **PlanningStart** must be converted to **UTC**.  
> - A critical activity area is one with workload **greater than 100**.  
> - In the summary, always specify the **critical areas** from **CheckingPickingWorkloadSituation**, and if **simulation** or **execution** is triggered, include the **summary of rebalanced resources**.  
> - Maintain a **clear**, **professional**, and **supportive tone**.  
> - The agent assists **warehouse supervisors** and **shift leads** in making **data-driven resource allocation decisions**.  
> - The communication style should emphasize **efficiency**, **accountability**, and **collaboration**.  
>  
>  **Communication Style**  
> - Maintain an **analytical** and **solution-oriented** tone.  
> - Present insights with **clear evidence** and **structured reasoning**.  
> - Provide **actionable** and **practical recommendations**.  
> - Use **structured responses** for maximum clarity and readability.

---

### 3. Select the Agent Model

| Field | Setting |
|--------|----------|
| **Model** | `Medium` |
| **LLM Provider** | `OpenAI` |
| **Base Model** | `GPT-4o Mini` |
| **Advanced Model** | `GPT-4o` |
| **Backup LLM** | Toggle **Off** |

In **Advanced Configuration**, check the box for **Post-processing**.

<img width="940" height="418" alt="image" src="https://github.com/user-attachments/assets/bff5c61c-eaed-4a4c-a68f-f13e1d3a00a6" />

---

### 4. Add Joule Skills as Tools

1. In the **Tools** section, click **Add Tool → Joule Skill**.  
2. A pop-up will display all available Joule Skills in your project.  
3. Select and add the following skills one by one:
   - `CheckingPickingWorkloadSituation`  
   - `SimulateWorkforceOptimization`  
   - `ExecuteWorkforceOptimization`

   <img width="940" height="421" alt="image" src="https://github.com/user-attachments/assets/db00ebe8-a3b1-4198-82cf-89fa02fc0e9d" />  
   <img width="940" height="196" alt="image" src="https://github.com/user-attachments/assets/d113fa6c-a875-41e2-9040-887d6a302b35" />

---

### 5. Add Document Tool

1. In the **Tools** section, click **Add Tool → Documents**.  
2. Enter the following details:  

   | Field | Value |
   |--------|--------|
   | **Tool Name** | `Warehouse Operations Management Document` |
   | **Description** | `Guidelines for Warehouse Operations Management App` |
   | **Destination Variable** | `AICore` |
   | **Resource Group ID** | `MFSResourceGroup` |
   | **Collection ID** | `620785a0-b5fa-4901-94be-2e194f926953` |

3. Click **Add**.  

   <img width="940" height="436" alt="image" src="https://github.com/user-attachments/assets/762e9804-604d-49e3-b0fb-f253ec37d136" />

---

### 6. Add Calculator Tool

1. In the **Tools** section, click **Add Tool → Calculator**.  
2. Enter the following details:  

   | Field | Value |
   |--------|--------|
   | **Tool Name** | `Calculator` |
   | **Description** | `Basic arithmetic operations for numeric data handling.` |

3. Click **Add**.  

   <img width="745" height="382" alt="image" src="https://github.com/user-attachments/assets/17bb8e9b-f63d-4f82-9463-eb75dfe11821" />

---

### 7. Save the Agent

Once all configurations are complete, click **Save** to finalize your Joule Agent.

---

✅ **Result:**  
You have successfully created the **Warehouse Workforce Optimization Agent**.  
This agent integrates multiple Joule Skills to autonomously analyze warehouse workloads, simulate or execute optimization actions, and provide meaningful, professional summaries to warehouse supervisors.

---

➡️ **Next Exercise:** [Exercise 6 – Test an Agent in a Private Environment](https://github.com/SAP-samples/teched2025-AD169/blob/main/exercises/ex6/README.md)
