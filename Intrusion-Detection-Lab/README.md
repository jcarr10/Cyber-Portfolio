# Network Intrusion Detection Using Snort

## Overview

This project demonstrates how an intrusion detection system (IDS) can be used to monitor and detect malicious network activity. 

The lab was performed in a virtual cybersecurity environment using Kali Linux and Snort to identify potential intrusion attempts and analyze network traffic.

The objective of this project was to simulate network attacks and detect them using signature-based intrusion detection rules.

## Tools Used

- Kali Linux
- Snort
- Wireshark
- VirtualBox
- SimSpace Cyber Range

## Lab Environment

The lab was conducted in a virtualized cybersecurity environment.

Operating System:
Kali Linux

Virtualization Platform:
VirtualBox

Cyber Range:
SimSpace Cyber Range

The virtual environment allowed for safe testing of intrusion detection techniques without impacting real systems.

## Attack Scenario

The objective of this lab was to simulate malicious activity within a controlled environment and detect it using Snort intrusion detection rules.

The IDS monitored network traffic and generated alerts when suspicious patterns were detected.

This simulation represents how security teams monitor enterprise networks for signs of compromise.

## Intrusion Detection Process

Snort was configured to monitor network traffic and detect suspicious activity based on predefined rules.

The IDS analyzes packets traveling across the network and compares them against known attack signatures.

When a matching pattern is detected, Snort generates an alert that security analysts can investigate.

## Example Snort Rule

Example rule used to detect suspicious SSH traffic:

alert tcp any any -> any 22 (msg:"Possible SSH intrusion attempt"; sid:1000001;)

This rule triggers an alert whenever traffic targeting SSH services is detected.

## Analysis

During the lab, Snort successfully detected simulated intrusion attempts and generated alerts for suspicious network activity.

The alerts allowed analysis of potential attack patterns and provided insight into how intrusion detection systems assist security teams in identifying threats.

## Security Implications

Intrusion detection systems play an essential role in monitoring networks and identifying potential cyber threats.

Organizations rely on IDS technologies to detect malicious behavior, investigate incidents, and strengthen their overall cybersecurity posture.

## Skills Demonstrated

- Network intrusion detection
- Cybersecurity monitoring
- Network traffic analysis
- IDS rule configuration
- Threat detection


