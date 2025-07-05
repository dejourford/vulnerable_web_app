# Vulnerable Web App Lab

+---------------+ +-------------+ +--------------+

| DejourPC | <---> | DVWA Server | <---> | SamanthaPC |

| (Domain Joined)  || (Ubuntu, non-AD)|| (Domain Joined)|

+---------------+ +-------------+ +---------------+


## Scenario
After creating a small enterprise network for a new startup, Ford Trucking Company, and two of its first employees, you are now tasked with setting up an internal company server running a vulnerable web app application (DVWA).

## Requirements

1. The vulnerable web app to be used is DVWA (Damn Vulnerable Web App)
2. The web app should be installed on an Ubuntu Server VM
3. The DVWA server must:
    - Not be domain-joined
    - Be reachable internally (e.g., via static IP like 10.10.2.20)

## What I Did

## Lessons Learned

## Future Improvements
- Add a Kali Linux attacker VM and test DVWA vulnerabilities
- Use Wireshark to capture login or attack attempts
- Deploy SIEM (like Wazuh) to monitor activity from the DC or a logging server

    
