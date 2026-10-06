# Active Directory Security Monitoring Lab

## Overview

This project demonstrates a small Windows Active Directory home lab built for blue-team practice.

The goal of the lab is to understand how Windows authentication activity is generated, logged, collected, and investigated from a SOC analyst perspective.

## Lab Environment

- Debian host
- QEMU/KVM
- Windows Server Domain Controller
- Windows client
- Kali Linux
- Wazuh SIEM

## What I Built

- Configured a Windows Active Directory lab
- Deployed a Domain Controller
- Connected Windows telemetry to Wazuh
- Investigated Windows Security events in Event Viewer and Wazuh
- Practiced identifying authentication-related activity
- Compared raw Windows events with SIEM data
- Used Kali Linux as a separate testing machine inside the lab network

## SOC Workflow

1. Generate authentication activity in the lab
2. Review the event on the Windows system
3. Locate the same event in Wazuh
4. Inspect important fields such as:
   - Event ID
   - Username
   - Source IP
   - Logon type
   - Failure reason
   - Timestamp
5. Correlate the activity with the surrounding events
6. Document the findings as a SOC investigation

## Skills Demonstrated

- Active Directory fundamentals
- Windows Security Event Logs
- SIEM monitoring with Wazuh
- Basic threat detection
- Log analysis
- Authentication event investigation
- Linux / Windows lab administration
- Virtual networking
- Blue-team investigation workflow

## Screenshots

Add your strongest screenshots here:

### 1. Active Directory / Domain Controller
![Active Directory](screenshots/01-active-directory.png)

### 2. Windows Security Event
![Windows Event](screenshots/02-windows-security-event.png)

### 3. Wazuh Detection / Event Investigation
![Wazuh](screenshots/03-wazuh-event.png)

### 4. Lab Infrastructure
![Lab](screenshots/04-lab-infrastructure.png)

## What I Learned

This lab helped me understand the full path from Windows activity to SIEM visibility.

Instead of only reading about authentication logs, I worked with the events directly, inspected their fields, and used Wazuh to investigate the same activity from a SOC analyst perspective.

The most useful part of the project was learning how to move from a raw security event to an analyst question:

**What happened, which account was involved, where did the activity come from, and is it suspicious?**

## Next Improvements

- Add custom detection rules
- Add more Windows authentication scenarios
- Create incident timelines
- Map selected detections to MITRE ATT&CK
- Add a short incident report for each scenario

## Disclaimer

This project was created in an isolated home lab for educational and defensive security purposes only.
