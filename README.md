# SOC Network Investigation & Log Correlation

## Overview

This project documents a hands-on Blue Team / Security Operations Center (SOC) investigation completed as part of CodePath's Intermediate Cybersecurity (CYB102) program.

The investigation focused on suspicious email activity within a simulated corporate environment. The objective was to determine the source of the activity and identify the device and user account associated with it by correlating evidence across multiple network and system data sources.

The investigation followed a structured SOC workflow using network packet analysis, DHCP records, and host security logs to trace suspicious activity from a network event back to a specific endpoint and user.

## Investigation Process

### 1. PCAP & SMTP Traffic Analysis

I used **Wireshark** to analyze a packet capture (PCAP) containing network traffic from the simulated environment.

SMTP display filters were applied to isolate email-related communications and identify network activity relevant to the investigation.

Analysis of the captured traffic identified the source IP address associated with the suspicious email activity.

### 2. DHCP Log Correlation

After identifying the source IP address, I analyzed **DHCP logs** to determine which device had been assigned that IP address during the relevant timeframe.

This step connected the network-level evidence discovered in Wireshark to a specific host within the environment.

### 3. Security Log Analysis

I then analyzed security logs from the identified host to investigate user authentication activity.

Login events were correlated with the timeline of the suspicious email activity to determine which user account was active during the event.

### 4. Event Correlation

Evidence from multiple data sources was combined to reconstruct the activity:

**Suspicious Email → SMTP Traffic → Source IP → DHCP Records → Host Identification → Security Logs → User Account**

This demonstrated how SOC analysts can correlate network and endpoint evidence to establish context around suspicious activity and determine which systems and users may be associated with a security event.

## Tools & Technologies

- Wireshark
- PCAP Analysis
- SMTP
- DHCP Logs
- Security/Event Logs
- Network Protocol Analysis
- Log Correlation

## Skills Demonstrated

- SOC Investigation
- Network Traffic Analysis
- PCAP Analysis
- Wireshark
- SMTP Traffic Analysis
- DHCP Log Analysis
- Security Log Analysis
- Event Correlation
- Incident Investigation
- Evidence Analysis
- Timeline Analysis
- Blue Team Methodology

## Key Takeaways

This project strengthened my understanding of how security investigations often require analysts to correlate evidence across multiple data sources rather than relying on a single alert or log.

By combining packet capture analysis, network addressing information, DHCP records, and host security logs, I was able to trace suspicious activity from the initial network event to the associated endpoint and user account.

The investigation reinforced a fundamental SOC analysis process:

**Detect → Investigate → Correlate → Identify → Document**

This methodology is applicable to security monitoring, incident triage, network investigations, and other Blue Team/SOC operations.

## Disclaimer

This project was completed in an authorized educational lab environment as part of CodePath's Intermediate Cybersecurity (CYB102) program. All network traffic, logs, systems, and investigative activities were provided or performed for cybersecurity education and defensive security training.
