# creating-a-backdoor-with-SET
creating a backdoor with SET - Ethical Hacking Techniques course

# AIM:
To Create a backdoor with Social Engineering Toolkit (SET)

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode


### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

### Architecture Diagram

```
+----------------+        +------------------------+        +----------------------+
| Attacker's PC  | -----> | SET (Credential        | -----> | Fake Login Page      |
| (Kali Linux)   |        | Harvester via Apache)  |        | (Hosted by SET)      |
+----------------+        +------------------------+        +----------------------+
       |                                                             |
       |                                                             v
       |   1. Configure SET with phishing site (e.g., Gmail clone)   |
       |                                                             |
       |                                                             v
       |                                                 +----------------------+
       |                                                 | Victim's Browser     |
       | <------------------------------------------------| Clicks Phishing Link|
       |                                                 +----------------------+
       |                                                             |
       |                                                             v
       |     2. Victim Enters Credentials → Sent to SET/Attacker    |
       |                                                             |
       |                                                             v
       |                                                 +----------------------+
       |                                                 | Credentials Captured |
       |                                                 | in Apache log/SET DB |
       |                                                 +----------------------+

```

## EXECUTION STEPS AND ITS OUTPUT:
Social Engineering attacks are the various cons used by the hackers to trick people into providing sensitive data to the attackers.

**Steps to Use SET for Phishing (Credential Harvester Attack Method)**

**1. Open terminal:**
```bash
sudo setoolkit
```
<img width="821" height="772" alt="7 1" src="https://github.com/user-attachments/assets/a5e31a58-3bc0-47cf-8a8e-62be8427c68f" />



**2. Navigate:**
```bash
1) Social-Engineering Attacks  
2) Website Attack Vectors  
3) Credential Harvester Attack Method  
```
<img width="825" height="617" alt="7 2" src="https://github.com/user-attachments/assets/f0dd1a8f-cc15-470a-8e7e-e6b028897d38" />
<img width="826" height="753" alt="7 3" src="https://github.com/user-attachments/assets/f257adfa-ce54-495f-a8a3-b70e53aada28" />



**3. Enter your IP address as the attacker server.**
**4. Choose:**
```bash
2) Site Cloner
```
<img width="825" height="347" alt="7 4" src="https://github.com/user-attachments/assets/248e8f88-f949-4352-99b7-9ec144c34fbd" />



**5. Enter the URL of the legitimate site ```(e.g., https://accounts.google.com)```**
<img width="823" height="286" alt="7 5" src="https://github.com/user-attachments/assets/b189e5c1-15f2-4351-a6e1-1d06a838772e" />



**6. Send the generated link to the victim.**
<img width="825" height="576" alt="7 6" src="https://github.com/user-attachments/assets/388962c9-cdd3-43b4-95f9-a148f5c836dd" />




**7. Once the victim logs in → their credentials are stored in:**
```bash
/var/www/html/
```
<img width="817" height="352" alt="7 7" src="https://github.com/user-attachments/assets/aafbe6a5-128c-46fa-9dea-dabf94e2202f" />




## RESULT:
The Social Engineering Toolkit (SET) is used to create backdoor is  examined successfully
