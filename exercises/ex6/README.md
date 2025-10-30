## Exercise 6 – Test an Agent in a Private Environment

### ⚙️ Context and Purpose
In [**Exercise 2 – Create a Private Environment for Testing**](https://github.com/SAP-samples/teched2025-AD169/tree/main/exercises/ex2/README.md), you created your **Private Environment**, which provides a safe, isolated space to test and refine your Joule Agent before deploying it to a shared environment.

Now that your **Warehouse Workforce Optimization Agent** is configured, it’s time to test it directly in your Private Environment to ensure that all skills, connections, and logic behave as expected.

---

### 🚀 Why This Matters
Testing in a **Private Environment** allows you to:
- Safely verify your agent’s logic and skill orchestration.  
- Ensure API destinations and Joule Skill connections work correctly.  
- Identify and fix configuration or data-mapping issues early.

This step confirms that your **Agentic Warehouse Operations** scenario functions correctly before release and deployment.

---

### 1. Launch the Test Session

Click on the **Test** button in the upper-right corner in Joule Studio.  
  <img width="1905" height="675" alt="image" src="https://github.com/user-attachments/assets/cda19b8b-4715-4444-9c07-e6adc99e2e88" />


---

### 2. Configure Test Parameters

In the **Test Setup** window, enter the following details:

| Parameter | Value |
|------------|--------|
| **Environment** | Select your environment associated with your user ID |
| **AICore** | `document-grounding` |
| **WHSOPMNG_DEST** | `zewm-autonomous-warehouse-agent-srv-api` |

Click **Continue** to start your testing session.

---

### 3. Interact with the Joule Assistant

#### 🧠 Prompt 1 – Run a Simulation
**Prompt:**
```Could you please assist me in verifying the critical activity areas in terms of workloads for warehouse TSEB for today using 7AM as planning start? In case critical areas exist, only simulate optimal resource allocation.```


**Expected Result:**  
The agent identifies critical activity areas and triggers a **simulation** for optimal workforce allocation.  
Rebalanced resources should be displayed.

![Simulation Result](https://github.com/user-attachments/assets/1665026b-b3cb-44da-8f2b-a4310ba601f1)

---

#### 🔍 Prompt 2 – Analyze Workloads Only
**Prompt:**

```Could you please assist me in verifying the critical activity areas in terms of workloads for warehouse TSEB for today using 6AM as planning start?```


**Expected Result:**  
The agent returns three critical activity areas — `T010`, `T151`, and `T152` — without triggering optimization.

![Workload Result](https://github.com/user-attachments/assets/38b85b95-a3ee-4840-8aae-82b566545e91)

---

### ✅ Result
You have successfully:
- Tested the **Warehouse Workforce Optimization Agent** in your Private Environment.  
- Verified that it correctly analyzes workloads, identifies critical areas, and performs simulations.  
- Ensured that API destinations and Joule Skills are functioning as expected.  


---

### 🎉 Congratulations!
You’ve successfully completed the **end-to-end Agentic Warehouse Operations scenario** — from creating actions and skills, to building an autonomous Joule Agent, and finally testing it in your private environment.  

Your agent can now intelligently analyze workloads, simulate optimizations, and support real-time operational decision-making in a production-ready setup.  

🏁 **You’re now ready to build, extend, and scale your own Joule Agents across enterprise domains!**

>  If you’d like to explore the **full agent lifecycle** — including how to release, deploy, and test your agent in a shared environment — continue to the next exercise.
>   
> ➡️ **Next Exercise:** [**Exercise 7 – Release, Deploy, and Test the Agent in a Shared Environment**](https://github.com/SAP-samples/teched2025-AD169/blob/main/exercises/ex7/README.md)
