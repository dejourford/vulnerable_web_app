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

1. Download Ubuntu Server ISO
<img src="/images/download_ubuntu_server.png" alt="" width=600/>

2. Create Virtual Machine
<img src="/images/create_virtual_machine.png" alt="" width=600/>

3. Install Ubuntu Server and set up DVWA
<img src="/images/install_ubuntu.png" alt="" width=600/>

4. Configured networking manually without netplan or dhclient

5. Assigned a static IP to enp0s8 (host-only adapter)

6. Installed necessary software (Apache2, MariaDB)

7. Cloned DVWA Repo
    
    [cd /var/www/html]
    
    [sudo git clone https://github.com/digininja/DVWA.git]
    
    [sudo chown -R www-data:www-data DVWA]

8. Configured MariaDB
    - Created DVWA Database
    - Granted privileges to user root@localhost

9. Accessed DVWA from via browser
<img src="/images/access_dvwa.png" alt="" width=600/> 

## Lessons Learned
- NAT Adapter is needed for internet access to set everything up properly
- Had to manually set the IP address since dhclient wouldn't work due to being deprecated
- Copy and pasting wouldn't work which prevented the use of netplan since syntax is important

## Future Improvements
- Add a Kali Linux attacker VM and test DVWA vulnerabilities
- Use Wireshark to capture login or attack attempts
- Deploy SIEM (like Wazuh) to monitor activity from the DC or a logging server

    
