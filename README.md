# SOC-Network-Investigation-PCAP-Log-Correlation-Project
This project documents a Blue Team/Security Operations Center (SOC) investigation completed as part of CodePath's Intermediate Cybersecurity (CYB102) program.
The scenario involved investigating suspicious email activity within a simulated corporate environment and determining whether a user had been impersonated. The investigation required correlating evidence across multiple network and system data sources to identify the device and user associated with the activity.     
Using Wireshark, I analyzed a PCAP containing network traffic and applied SMTP display filters to isolate relevant email communications. The investigation identified the source IP associated with the suspicious activity.     CYB102 UNIT 1 LAB
I then correlated the identified IP address with DHCP logs to determine which host had been assigned that address during the relevant timeframe.    
Finally, I analyzed system security logs from the identified host and correlated login activity with the timeline of the suspicious email activity to determine which user account was active.     C

Skills demonstrated: Network traffic analysis, PCAP analysis, Wireshark, SMTP analysis, DHCP log analysis, security log analysis, event correlation, incident investigation, evidence analysis, and Blue Team/SOC methodology.
