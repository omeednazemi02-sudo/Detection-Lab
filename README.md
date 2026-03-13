# Detection Lab

## Objective
The Detection Lab project established a virtualized cybersecurity environment designed to simulate and detect real-world attack activity. Using VMware Workstation Pro, multiple Ubuntu virtual machines were deployed to replicate a basic Security Operations Center (SOC) monitoring architecture. The lab focused on implementing a Wazuh SIEM platform, generating attack telemetry through simulated SSH brute-force attempts, and analyzing authentication logs to detect malicious behavior. The goal was to demonstrate how security monitoring tools identify attack patterns and enable incident response actions such as blocking malicious IP addresses.

### Skills Learned

- Deployment of a virtual cybersecurity lab environment using VMware Workstation Pro.
- Installation and configuration of Ubuntu Linux as the operating system for multiple virtual machines.
- Creation and management of multiple virtual machines to simulate a SOC monitoring environment.
- Installation and configuration of a Wazuh SIEM platform on Ubuntu Linux.
- Configuration of Wazuh agents for endpoint monitoring and centralized log collection.
- Understanding of Linux authentication logs and SSH security monitoring.
- Detection and analysis of SSH brute-force login attempts through SIEM alerts.
- Investigation of security events to identify attacker IP addresses and authentication patterns.
- Implementation of incident response actions by blocking malicious IP addresses using firewall rules (iptables).
- Practical experience simulating real-world attack scenarios in a controlled cybersecurity lab environment.

### Tools Used

- Wazuh SIEM for log collection, monitoring, and threat detection.
- VMware Workstation Pro to create and manage a virtualized SOC lab environment.
- Ubuntu Linux as the operating system for the SIEM server, monitored endpoint, and attacker machine.
- OpenSSH to simulate remote login attempts and generate authentication logs.

## Steps

### Step 1 – Wazuh Installation

The Wazuh SIEM platform was installed on an Ubuntu virtual machine using elevated privileges in the terminal. This machine serves as the primary monitoring server for the detection lab environment.

<img width="1000" height="500" alt="image" src="https://github.com/user-attachments/assets/029c67e2-c64c-4a2f-b47e-922c5facc11d" />



---

### Step 2 – Wazuh Dashboard Access

After installation, the Wazuh dashboard was accessed through the browser interface. This dashboard provides visibility into alerts, system health, and threat detection across monitored endpoints.

<img width="1000" height="500" alt="image" src="https://github.com/user-attachments/assets/769df6e8-9f27-437f-845c-b89f695e9609" />



---

### Step 3 – SSH Service Configuration

SSH was enabled on the monitored Ubuntu endpoint to allow remote login attempts. This service generates authentication logs that can be monitored by the SIEM platform.

<img width="1000" height="500" alt="image" src="https://github.com/user-attachments/assets/d521457c-4b53-4b13-8ff2-534fe95b1ce2" />



---

### Step 4 – Attack Simulation

A third Ubuntu virtual machine was created to simulate an attacker system. Multiple SSH login attempts were performed using incorrect credentials to simulate a brute-force attack.

<img width="1000" height="500" alt="image" src="https://github.com/user-attachments/assets/52ac9c45-7fb9-46bc-a9a3-088a9690569f" />



---

### Step 5 – Threat Detection

The Wazuh SIEM server detected repeated authentication failures and generated alerts indicating attempts to log in using a non-existent user.

<img width="1000" height="500" alt="image" src="https://github.com/user-attachments/assets/3efdae13-2b99-4e75-b2fc-cbe22d03f87e" />



---

### Step 6 – Log Investigation

The Wazuh event details were analyzed to investigate the attack. By examining the log data, the source IP address of the attacker machine was identified.

<img width="1000" height="500" alt="image" src="https://github.com/user-attachments/assets/6febb340-5dd3-4108-b123-848f70d69cac" />



---

### Step 7 – Incident Response

After identifying the malicious source IP address, a firewall rule was implemented on the monitored endpoint using iptables to block the attacker.

<img width="1000" height="500" alt="image" src="https://github.com/user-attachments/assets/d391dcdf-6ea0-4517-b5ee-6ea6e2816cec" />


---

### Step 8 – Attack Mitigation Verification

After applying the firewall rule, the attacker machine was no longer able to establish an SSH connection to the monitored endpoint, confirming the successful mitigation of the attack.

<img width="1000" height="500" alt="image" src="https://github.com/user-attachments/assets/010eeb0d-1d81-41d4-b178-6ce65a887c31" />
