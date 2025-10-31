## Exercise 3: Copy the Project ‘WarehouseOperationsManagement’ 

## 💡 Pre-Delivered Joule Skills

Since the hands-on session has limited time, we have already prepared a few **Joule Skills** for you as part of the **Warehouse Agent** setup.  
These pre-delivered skills use the **same SAP Build Action project**, allowing you to focus on exploring how Joule integrates with backend processes rather than building everything from scratch.


Here’s what the two existing skills do:

- 🧳 **Check Workload Situation**  
  This skill retrieves an overview of the **current workload** across different **activity areas** in the warehouse.  
  It helps supervisors understand where workload imbalances exist — for example, identifying areas that are over- or under-utilized — so they can make better staffing decisions.

- 🕵🏻‍♀️ **Assign Single Resource to Activity Area**  
  This skill allows supervisors to **assign an individual worker (resource)** to a specific **activity area** based on the current workload data.  
  It streamlines the manual assignment process and ensures that resources are distributed efficiently to meet operational needs.

And here’s a quick reminder of how your **final Joule Agent** will look once all the skills are connected:
<p>
  <img src="https://github.com/SAP-samples/teched2025-AD169/blob/main/images/Agent%20for%20Warehouse%20Operations.jpeg" width="800" alt="Agent for Warehouse Operations"/>
</p>

## 🧩 Copy the Project ‘WarehouseOperationsManagement’ 


### Step 1: Save *WarehouseOperationsManagement* as a New Project

As mentioned earlier, some of the **Joule Skills** were pre-created for this hands-on session.  
You’ll begin by **copying the existing project** so that you can safely add a new Joule Skill within the same setup.

Follow these steps:

👉 1. In **SAP Build Lobby**, in the project list, locate the WarehouseOperationsManagement project

👉 2. Click on the arrow icon (›) on the right side of the row to open the project details page
   <img width="1562" height="526" alt="image" src="https://github.com/user-attachments/assets/036d640f-4cc1-408e-83c1-c13caab14fa7" />

👉 3. On the right-side panel, open the **Versions** tab
👉 4. Click the **three dots (⋮)** next to *Editable* and then click the **Save As New** button to create your personal copy
   
   <img width="1696" height="835" alt="image" src="https://github.com/user-attachments/assets/e0913212-f3e6-496e-aac9-e2f211b20ce5" />

### Step 2:  Provide Unique Name with your User ID

A unique name is required since there are many workshop attendees, and you need to be able to easily locate your own project.

👉 1. Provide the name of the new project as: ```WarehouseOperationsManagement_<userid>``` (replacing <userid> with your user ID)
   <img width="1576" height="660" alt="image" src="https://github.com/user-attachments/assets/51348f6d-8974-45a2-9906-3e128b1b660d" />

👉 2. Click on ‘Save As New’ button to save your personal version
   <img width="1576" height="660" alt="image" src="https://github.com/user-attachments/assets/23f016dd-62c9-458b-b6c4-cea852da3892" />


### Step 3: Review the Project

👉 Once the project is saved, open it by clicking on its name in the SAP Build Lobby 
   You should now see two **pre-created Joule Skills** that are already part of this project:

- `AssignSingleResourceToActivityArea`  
- `CheckingPickingWorkloadSituation`

<br>

  <img width="1689" height="775" alt="image" src="https://github.com/user-attachments/assets/95b4b0e0-ab2f-4170-9d49-ce91d99d7d7c" />



## 🌟 What's Next

Now that your Joule Studio project is set up, it’s time to **create your first Joule Skill**.  
This new skill will extend the existing project and connect to the same SAP Build Action used by the pre-created skills.

➡️  [Next Exercise - > Exercise 4 - Create a New Joule Skill](https://github.com/SAP-samples/teched2025-AD169/blob/main/exercises/ex4/README.md)


