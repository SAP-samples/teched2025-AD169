# Exercise 1 - Test the Action Project

There is an action project which will be used in this hands-on project for Joule skill creation. The action project is already created. In this section, let us test the action project.
<br>1: In the left panel of the lobby area, expand ‘Connectors’ and click on ‘Actions’
<br>2: Search for the action project, ‘WarehouseWorkloadDetermination’. Click on it to open

<br> <img width="940" height="374" alt="image" src="https://github.com/user-attachments/assets/ab1723c9-cc76-4cd0-8927-30a36ce27b3c" />


<br>3: 	Click on the Test tab.
<br>Provide the below input parameters to test the action
 <br> . “warehouse": "TSEB",
 <br> . "is_simulation": true,
 <br> . "planning_start": "2025-10-15T00:00:00Z",
 <br> . "planning_horizon_to": "2025-10-16T00:00:00Z",
 <br> . "planning_horizon_from": "2025-10-15T00:00:00Z"
 <br> .  Choose the destination as ‘zewm_autonomous-warehouse-agent-srv-api’ 
 <br> <br> Click on Test button
<br><img width="940" height="405" alt="image" src="https://github.com/user-attachments/assets/97668dfc-678d-44c9-ad5e-feacee11c305" />
<br> <br> Result: Response should be ‘200 OK’
<br><img width="940" height="471" alt="image" src="https://github.com/user-attachments/assets/fefe3469-cd5d-4923-b5eb-6c274a9afcd4" />

<br>Let us use this Action in the next section of the exercise while creating the Joule Skill
