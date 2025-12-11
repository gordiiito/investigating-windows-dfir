Investigating Windows – DFIR Case Report

This repository contains a host-based forensic investigation of a compromised Windows Server 2016 machine. The objective of this project was to identify attacker activity, persistence mechanisms, credential access, and indicators of compromise. All analysis was performed manually using built-in Windows tools.

The full report is located in the report folder. Screenshots and supporting evidence used in the investigation are stored under evidence/screenshots.

Summary

The investigation identified:

– A malicious Registry Run key executing remote commands
– A scheduled task used for persistence
– Evidence of credential dumping with mim.exe (Mimikatz)
– DNS modifications pointing to an attacker-controlled IP
– Unauthorized firewall rule changes
– Web shell files placed in the IIS webroot
– Privileged accounts created or modified by the attacker

These findings indicate full system compromise requiring reimaging and credential resets.
