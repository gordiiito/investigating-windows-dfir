Investigating Windows – DFIR Case Report

This repository contains a host-based forensic investigation of a compromised Windows Server 2016 machine. The goal of this project was to identify evidence of attacker activity, persistence mechanisms, credential access, and indicators of compromise. All analysis was performed manually using built-in Windows tools.

The full report is located in the report folder. Screenshots and supporting evidence used in the investigation are stored under evidence/screenshots.

Repository Structure

report
 Investigating_Windows_Report.pdf

evidence
 screenshots
  01_systeminfo.png
  02_getlocaluser.png
  03_John_last_login.png
  04_registry_updatesvc.png
  05_admin_group.png
  06_scheduled_task.png
  07_task_actions.png
  08_jenny_user.png
  09_compromise_date.png
  10_mimikatz.png
  11_hostsfile_c2ip.png
  12_webshell_jsp.png
  13_firewall_rule.png

Summary

The investigation identified the following:

– A malicious Registry Run key executing remote commands
– A scheduled task used for persistence
– Evidence of credential dumping with mim.exe (Mimikatz)
– DNS modifications pointing to an attacker-controlled IP
– Unauthorized firewall rule changes
– Web shell files placed in the IIS webroot
– Privileged accounts created or modified by the attacker

These findings indicate full system compromise requiring reimaging and credential resets.