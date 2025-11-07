# Phishing-Simulation (Microsoft Defender) 
Quick description: A simple phishing simulation built with Microsoft Defender for Office 365 Attack simulation & training. The goal is to safely measure user susceptibility to credential-harvest phishing and automatically assign training to those who fall for it.


# why I built this? 
Phishing is the most common initial access vector. This project shows how to run a targeted simulation in Microsoft Defender, measure results, and provide trainings in an  organisation.

# Objective 
Run a credential harvest phishing simulation, measure clicks and credential rates, and automatically assign training to users who interacted with the phishing email. Capture logs/screenshots for reporting and learning.


# Prerequisites
- Microsoft Defender for Office 365 with Attack simulation & training enabled.
- Test user accounts


# Steps by step (what I did)


1. In the Microsoft Defender portal,go to Email & collaboration → Attack simulation & training.
<img width="2874" height="1460" alt="Screenshot 2025-11-06 121714" src="https://github.com/user-attachments/assets/cfdee2d5-913f-400b-891f-7003532f5e2d" />

2. Click Create campaign and choose a campaign name
3. Set the attack type to Credential harvest, (we want to test whether users will submit credentials)
<img width="2874" height="1248" alt="Screenshot 2025-11-06 121944" src="https://github.com/user-attachments/assets/c6d45c04-e4ce-4ec9-aca9-1123a59b1a25" />

4. Choose a payload template, I chose "Expense report sharing" because of the Predicted compromise rate was highest (40%).
<img width="2880" height="1364" alt="Screenshot 2025-11-06 122118" src="https://github.com/user-attachments/assets/77315b47-eb26-4d29-bfb2-07e27ecb4d03" />

5. Select target users. For this run I included All users
<img width="2880" height="1366" alt="Screenshot 2025-11-06 124129" src="https://github.com/user-attachments/assets/9b2c719f-ad2c-47bf-ac54-14409cc408e4" />

6. Assign training to users who fail the simulation. I used Microsoft’s built in training to keep the workflow simple and repeatable. You can also upload a custom course.
<img width="2880" height="1442" alt="Screenshot 2025-11-06 124207" src="https://github.com/user-attachments/assets/c78de0b2-37db-430a-8166-739d85d9972c" />


7. Configure notification options (default post simulation notification was used) and scheduling (launch now or schedule). I used the default notify setting and launched the campaign immediately.
<img width="2876" height="1462" alt="Screenshot 2025-11-06 124400" src="https://github.com/user-attachments/assets/d124e764-cec2-4645-80f0-ea04f58c895a" />



# Outcome  
Once the simulaion was lunched, I checked one of the users email addresses and clicked on the phishing email that was sent earlier and provided the credentials just to test it out. 

- The campaign launched successfully.
- I used a test user to validate behaviour. Their inbox received the phishing message, clicked the link, and submitted credentials on the simulated page (test credentials provided intentionally to verify the flow).

<img width="2880" height="1650" alt="Screenshot 2025-11-06 124602" src="https://github.com/user-attachments/assets/4a977e12-8f0c-41aa-8309-6a349aaa293e" />

<img width="2880" height="1622" alt="Screenshot 2025-11-06 124644" src="https://github.com/user-attachments/assets/7e4943d5-bdd5-470e-a672-6cfb8b4546f7" />


<img width="2844" height="1438" alt="Screenshot 2025-11-06 124714" src="https://github.com/user-attachments/assets/a9986913-b768-4b35-a8a0-4a3ebfe4f219" />


# Simulation Summary

- Total users targeted: 3

- Compromised users: 1 (33.33%)

- Users who reported the email: 0 (0%)

- Training completion rate: 0% (training not yet started)

- Average time to first click: 46 seconds

<img width="2880" height="1468" alt="Screenshot 2025-11-06 125113" src="https://github.com/user-attachments/assets/a4884f9e-3ad4-4a10-8639-2667b41efa3e" />





# Detailed User Activity

Selecting Jenny Smith reveals the timeline of her actions during the simulation:

- 11:50:21 — Clicked the message link

- 11:50:25 — Read the phishing message

- 11:51:03 — Supplied credentials on the phishing landing page

This confirms that the phishing simulation successfully detected and logged credential submission activity.

<img width="2878" height="1460" alt="Screenshot 2025-11-06 125239" src="https://github.com/user-attachments/assets/163bb4b2-b2c6-488e-a9db-71be19d3a6fd" />



# Key Takeaways

The campaign successfully simulated a real world credential harvest phishing attempt.

Microsoft Defender accurately tracked user interactions and marked compromised accounts.

Follow up training was automatically assigned to the compromised user to reinforce phishing awareness.

This type of controlled phishing simulation is essential for measuring organisational readiness and strengthening security culture.
