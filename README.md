<h1>Azure SOC</h1>


<h2>Description</h2>
Created a mini Security Operations Center (SOC) by using resources available in Microsoft Azure to detect Indicatiors of Compromise (IOCs) which are sent to a Security Information and Event Manager (SIEM) to overlook potentially malicious activity in the personal lab.
<br />


<h2>Tools</h2>

- <b>Microsoft Azure</b> 
- <b>Microsoft Sentinel SIEM</b>

<h2>Lessons Learned </h2>

- <b>SIEM configuration through data connection.</b>
- <b>Task automation as to configuring alerts to trigger when certain criteria is met.</b>
- <b>Incident monitoring.</b>

<h2>Project Walkthrough:</h2>

**Step 1:** Created personal Virtual Machine (VM) with Remote Desktop Protocol (RDP) inbound traffic allowed through port 3389. In addition, created a resource group to house all of the resources for the project including the VM.

<img width="952" alt="longovm" src="https://github.com/user-attachments/assets/d8bfa386-2399-4502-b279-b1cc656c91d6">

<br>

**Step 2:** Created Log analytics workspace then added the VM and Sentinel SIEM to the workspace.

<img width="956" alt="longologanalyticswork " src="https://github.com/user-attachments/assets/6898b3d4-2a8e-4370-b38f-081e83e68248">

<br>

**Step 3:** Configured data connector in Sentinel for Windows Security Events to be logged into the SIEM.

<img width="954" alt="securityeventtosentinel" src="https://github.com/user-attachments/assets/11b0277e-d617-4cb2-8c4c-02d7a2b7533e">

<br>

**Step 4:** Created a real time successful local sign-ins rule.

<img width="951" alt="createdseceventrule" src="https://github.com/user-attachments/assets/8f2a7b84-90cb-4c66-88e5-5087efad955b">

<br>

**Step 5:** Signed in using RDP and an incident was created due to the rule that was created in Step 4.

<img width="950" alt="incidentsgen" src="https://github.com/user-attachments/assets/14a8d9c4-9056-4b9d-a9e6-eeeadcdaff15">
