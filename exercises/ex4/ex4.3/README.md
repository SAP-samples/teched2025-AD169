## Exercise 4.3 – Add a Send Message in Joule Skill

In this exercise, you will add a **Send Message** step to your Joule Skill.  
This step allows you to define how simulation results are displayed — giving you, as a developer, **complete control over the output structure, layout, and data presentation**.  
Although Joule can already display the skill output independently, the **Send Message** step is used when you need to customize **exactly how** that output appears to the end user.

---

### ⚙️ Why You Need to Design the Send Message

By default, **Joule** can show the response returned from a Joule Skill automatically.  
However, in many real-world use cases, you might want to **control how that output is formatted** — for example, presenting data as a structured list, table, or message card.  
Adding a **Send Message** step allows you to define that experience precisely through the **Message Editor**.

You would design a **Send Message** when:
- You want **full flexibility** in customizing the response format and presentation.  
- You need to **map backend data** (from the action output) into a structured or visual display.  
- You want to provide a more **guided, business-readable** summary directly in Joule.

> 💬 **Design Tip**  
> If your Joule Skill is **only called by a Joule Agent**, or if the **output format is not important** for your use case, you can skip this section.  
> The agent will automatically handle result summarization and conversational output.

---

### 1. Add a Send Message Step

1. Below the **Action call**, click on the **`+`** button and choose **Send Response → Send Message**.  

   <img width="940" height="461" alt="image" src="https://github.com/user-attachments/assets/297092e9-0f24-493a-8048-090cf9c1b817" />

2. On the right panel, change the step name to **Simulate Workload Message** and **Save**.

3. Click on **Open Message Editor**.  

   <img width="1611" height="562" alt="image" src="https://github.com/user-attachments/assets/72ab61e0-9ffc-4c2c-825d-fd930f58aeac" />


---

### 2. Configure the Message

<img width="1582" height="849" alt="image" src="https://github.com/user-attachments/assets/575e9ba4-d144-4665-a2b2-9d882ecb3fe4" />

4. In the **Edit User Interaction** pop-up, set the following:
   - Select **Message Type:** `List`
   - Write **Title:** `Simulated Optimization Results`
   - Write **Text:** `Workforce Optimization Results`

5. In the **List Item** section, click **Edit List Item**.  

   <img width="939" height="423" alt="image" src="https://github.com/user-attachments/assets/28bab2d7-47b1-4adb-b981-3bf72b53774c" />

6. In the **List Content** field, click the **`<>`** button to perform data mapping.  
   Expand the Joule Action Result section and map the **`value`** field.  

   <img width="940" height="455" alt="image" src="https://github.com/user-attachments/assets/c453aeb1-b250-4606-b437-9be2be8d9899" />

7. In the **Title** field, click **`<>`** and map  
   `Joule.Action.Result → value → Resource`.  

   <img width="1038" height="703" alt="image" src="https://github.com/user-attachments/assets/005e1841-f953-45d2-af41-7d63fed57b7d" />

8. In the **Text** field, click **`<>`** and map  
   `Joule.Action.Result → value → status_text`.  

   <img width="940" height="528" alt="image" src="https://github.com/user-attachments/assets/b9aab3ba-7398-4247-bb73-e39b8918db0c" />

9. In the **Status** field, click **`<>`** and map  
   `Joule.Action.Result → value → status`.  

   <img width="940" height="462" alt="image" src="https://github.com/user-attachments/assets/4dd20600-2640-4f1b-b218-735498aea174" />

10. In the **Detail View > Section Details**, set **Title:** `Optimization Details`
---

### 3. Add Attributes

11. In the **Attributes** section, click **Add Attribute** and create the following:  
 

   | Type | Label | Value (click on the `<>` button) |
   |------|--------|----------------------------------|
   | Text | `Resource` | `Joule.Action.Result → value → resource` |
   | Text | `Status` | `Joule.Action.Result → value → status` |
   | Text | `Activity Area` | `Joule.Action.Result → value → activity_area` |
   | Text | `Resource Type` | `Joule.Action.Result → value → resource_type` |

12. Click **Save** to confirm.  
    Once the details are added, the **Preview** should appear in the right panel.

   <img width="939" height="522" alt="image" src="https://github.com/user-attachments/assets/4b3f86a9-cd84-4926-a175-00626e4d7b22" />



---

✅ **Result:**  
You have now designed a custom **Send Message** step for your Joule Skill.  
While Joule can display output automatically, this approach gives you **full control** over how simulation results are formatted and presented.  
If the skill is only used by the **Joule Agent**, or output format is not relevant, this step can be skipped.

---

➡️ **Next Exercise:** [Exercise 4.4 – Configure the Output Parameter](https://github.com/SAP-samples/teched2025-AD169/blob/main/exercises/ex4/ex4.4/README.md)
