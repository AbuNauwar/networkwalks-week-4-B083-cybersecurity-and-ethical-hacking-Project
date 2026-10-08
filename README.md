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

Scope and Methodology

This project work covers pentest on the target website only (https://medirozahosptal.com ),the following activities and analysis were perform to ascertain vulnerability of the website and recommends ways to improve and mitigate such vulnerabilities professionally.

1.	Footprinting ( Recognisance) analysis
2.	Username enumeration on the login page to discover vulnerability of ether the username or password.
3.	Cracking of passwords on patients report on PDF files
4.	Decryption of PDF patient reports files 
5.	Accessed of backup folder with directory listing
6.	Accessed confidential and staff files and shareholders record on plain text

Methodology
However, the project adopt the use of some inbuilt Kalilinux tools such as Curl, the website was access using SQLInjection to bypass the password and maintain access on the website.

The cracking of password was achieved using networkwalks password cracker with a both small inbuilt wordlist and large wordlist for a complex password. The encryption of the PFDs was carried out using KaliLinux tool called QPDF.

Finally, the content of the backup folder (Old) was revealed with the help of an AI tool ( ChatGPT)

Risk Rating

Successful sqlInjection on the website, access to the forgotten backup folder, and access to confidential staff salary and shareholders information were considered to be most critical vulnerabilities of the website. While Encrypted PDFs accessible after login bypass and Weak PDF passwords crackable with a wordlist were also considered to be high vulnerabilities, and Sensitive metadata left in patient PDF files and username enumeration were considered medium vulnerabilities. 

Recommendations and Remediation

•	Username enumeration: Show the same error message for a wrong username and a wrong password. Never reveal which one failed.

•	SQL injection: Use parameterised queries or prepared statements. Never build SQL queries using raw user input.

 
•	PDF access control: Store PDFs outside the web root or behind proper access controls. Use strong unique passwords per file.

•	PDF metadata: Strip all metadata from patient files before distributing. Use exiftool -all= filename.pdf to clean files.

•	Directory listing and backup exposure: Disable directory listing on all folders. Remove or relocate old backup files. Never store database backups in a public web folder.






 
