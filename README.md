# networkwalks-week-4-B083-cybersecurity-and-ethical-hacking-Project

NETWORKWALKS
Mediroza General Hospital - Pentest Week 4 Project by Anas Muhammad Sani

Batch B082 | Week 4 | Confidential Target: https://medirozahospital.com

Penetration Testing Report

Executive Summary
#	Vulnerability	Location	Risk

1	Username enumeration on login page	patient/login.php	Medium

2	SQL injection login bypass	patient/login.php	Critical

3	Encrypted PDFs accessible after login bypass	patient/reports/	High

4	Weak PDF passwords crackable with a wordlist	patient_report_*.pdf	High

5	Sensitive metadata left in patient PDF files	patient_report_3.pdf	Medium

6	Forgotten backup folder with directory listing enabled	old/	Critical

7	Confidential staff salaries and shareholder data in plain text	old/mediroza_db_backup_2019.sql	Critical

 
