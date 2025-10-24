## Exercise 7 – Release, Deploy, and Test the Project in a Shared Environment

### ⚙️ Context and Purpose
In the previous exercise, you successfully tested your **Warehouse Workforce Optimization Agent** in a **Private Environment**.  
Now, it’s time to **release and deploy** your project to a **Shared Environment** — enabling collaboration, integration testing, and visibility for other users in the same tenant.

This step finalizes your work, ensuring that your Joule Agent is packaged, deployed, and functioning within the broader environment context.

---

### 🌍 Why This Matters
Releasing and deploying your project to a **Shared Environment** allows:
- Validation of the agent in a **multi-user** and **multi-system** setup.  
- Connection with shared **destinations** and external APIs.  
- End-to-end simulation of **Agentic Warehouse Operations** at scale.  

> 💡 **Good to Know:**  
> When your organization has Joule available in a **shared environment**, this same deployment flow will also apply when moving the project to **Joule in Production**.  
> The deployment process — including version release, environment selection, and destination mapping — follows the **same steps** as described below.

---

### 7.1 – Release and Deploy the Project

1. Open your **Project Overview** page in Joule Studio and click **Release**.  
   ![Release Button](https://github.com/user-attachments/assets/c230c7a4-f7d5-4782-a01c-f5a78efd1a86)

2. Once released, navigate to the **Released Version** of your project and click **Deploy**.  
   ![Deploy Button](https://github.com/user-attachments/assets/aed6cf09-2c6f-4649-9bdf-c847ee24beaf)

3. In the deployment dialog, select the **Shared Environment** created earlier in your tenant and click **Deploy**.  
   ![Select Environment](https://github.com/user-attachments/assets/e1ad4c23-a802-4fcc-b877-6699bdde994b)

4. Choose the destinations as follows:

   | Destination | Value |
   |--------------|--------|
   | **AICore** | `included-ai-core` |
   | **WHSOPMNG_DEST** | `zewm-autonomous-warehouse-agent-srv-api` |

   ![Destination Setup](https://github.com/user-attachments/assets/bc0dba7d-1806-4f51-be4e-7f733559a05b)

5. Click **Deploy**.  
   The project will begin deployment and show as **Deployed** once complete.  
   ![Deployed Status](https://github.com/user-attachments/assets/dfa6a698-7797-4221-af4f-2a701416d2af)

---

### 7.2 – Test the Deployed Project in the Shared Environment

1. Navigate to **Control Tower → Environments**.  
   ![Control Tower](https://github.com/user-attachments/assets/739717df-e7c6-4690-a3f6-dead30ceef21)

2. Search for and open the **Shared Environment** where your project was deployed.  
   ![Search Environment](https://github.com/user-attachments/assets/bc68312f-f73f-4226-8f6c-36531c996cfc)

3. Click on the **Joule** tab.  
4. Click **Launch** to open the **Joule Assistant**.  
5. Enter the same prompts used during testing in the **Private Environment** (see [Exercise 6 – Test an Agent in a Private Environment](https://github.com/SAP-samples/teched2025-AD169/blob/main/exercises/ex6/README.md)) to validate the behavior in the shared setup.

---

### ✅ Result
You have now:
- Released and deployed your **Warehouse Workforce Optimization Agent** to a shared environment.  
- Verified end-to-end agent behavior with shared API destinations.  
- Confirmed that the same process applies for **Joule Production Deployments**, ensuring consistency across environments.  
- Completed your **Agentic Warehouse Operations** setup, ready for collaborative and scalable use.



---

➡️ **Next Step:** [Return to the Exercise Overview](https://github.com/SAP-samples/teched2025-AD169.git)
