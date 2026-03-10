# Rogue Access Point Security Demonstration

## Overview
This was a self-initiated cybersecurity project that I developed to demonstrate how rogue wireless access points can be used to intercept or manipulate user traffic. I presented the project during a project fair to illustrate how easily attackers can create malicious Wi-Fi networks that appear legitimate.

## Objective
The goal of this project was to demonstrate the risks of connecting to unknown Wi-Fi networks and to show how attackers can exploit user trust in public or open wireless networks.

## Demonstration
During the demonstration I created a fake wireless access point designed to mimic a legitimate network. Once a device connected to the rogue access point, it was redirected to a fake Google login page.

This showed how attackers may:
- Trick users into connecting to a malicious Wi-Fi network
- Intercept or monitor traffic
- Redirect users to attacker-controlled pages

## Tools and Technologies
- Kali Linux
- hostapd
- dnsmasq
- Linux networking tools (tcpdump)

<img width="1327" height="748" alt="image" src="https://github.com/user-attachments/assets/1079d14d-363e-4a23-9bc0-00673c6089b6" />

In this screenshot, we can see the configuration implemented to perform the attack demonstration.

<img width="356" height="632" alt="image" src="https://github.com/user-attachments/assets/fd28ede7-a30d-4a2e-94b9-2419884c5f10" />

In this screenshot, we see the attack from the client’s perspective on their mobile device.

<img width="352" height="730" alt="image" src="https://github.com/user-attachments/assets/0d0b4295-6f7d-445c-b15e-001e2540bbaa" />

In this screenshot, the captive portal automatically prompts the user to sign in. The page mimics a Google login screen to demonstrate how attackers can use phishing pages on rogue Wi-Fi networks to capture credentials.

<img width="907" height="407" alt="image" src="https://github.com/user-attachments/assets/e0a2fcab-3ddd-4239-8795-0f7ee0282063" />

This screenshot shows the live feed of captured login attempts during the demonstration. The interface displays example credentials submitted through the phishing page to illustrate how attackers could collect sensitive information on a malicious Wi-Fi network.


## Skills Applied
- Wireless networking
- Linux system administration
- Traffic analysis
- Cybersecurity attack simulation
- Security awareness demonstration

## Key Takeaway
This project highlights how easily users can be deceived by a network that appears legitimate and reinforces the importance of verifying networks, using HTTPS, and avoiding unknown public Wi-Fi connections.

## Ethical Use
This project was conducted in a controlled environment for educational and demonstration purposes only.

## Future Implementation
The demonstration was originally built on a laptop running Kali Linux in a VMware virtual machine. A future improvement would be migrating the setup to a portable Raspberry Pi platform with a 7" touchscreen, battery pack, and custom 3D-printed case to create a self-contained demonstration device.

<img width="514" height="366" alt="image" src="https://github.com/user-attachments/assets/4a1bd48e-7d1b-4eb4-874b-c3510122d75f" />

In this screenshot, we can see the front of our custom Raspberri Pi setup.

<img width="508" height="429" alt="image" src="https://github.com/user-attachments/assets/e7030548-23b0-4a54-9abc-771c705d564b" />

In this screenshot, we can see the back of our custom Raspberri Pi setup.
