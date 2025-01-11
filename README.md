# CODETECH-TASK-4

#Name: Saurabh Yadav 
#Company:CODETECH IT SOLUTIONS 
#ID: CT0806GK 
#Domain: SQL 
#Duration: 12/12/24 to 12/1/25

Backup and Recovery Report Objective:

<img width="1296" alt="Screenshot 2025-01-11 at 7 02 00 PM" src="https://github.com/user-attachments/assets/c8abf527-d22c-46aa-a528-01f7a565bbc5" />
<img width="1296" alt="Screenshot 2025-01-11 at 7 02 16 PM" src="https://github.com/user-attachments/assets/f293a63e-4203-4be2-82d6-af25ace57efb" />
<img width="1296" alt="Screenshot 2025-01-11 at 7 02 54 PM" src="https://github.com/user-attachments/assets/6ff2ee5a-4515-4948-b0f2-e1708c7e8653" />
<img width="1296" alt="Screenshot 2025-01-11 at 7 03 40 PM" src="https://github.com/user-attachments/assets/f2033890-116a-4172-9231-0989d4372d62" />
<img width="1296" alt="Screenshot 2025-01-11 at 7 04 03 PM" src="https://github.com/user-attachments/assets/42f408a0-8178-4e4a-921d-60156a3f9dab" />
<img width="1296" alt="Screenshot 2025-01-11 at 7 05 18 PM" src="https://github.com/user-attachments/assets/99d7dc9a-f04b-47fb-9044-09e5c9598e7d" />





The objective of this task is to demonstrate the backup and recovery process for a database to ensure data availability and disaster recovery capabilities.
Backup Process
Step 1: Backup a MySQL Database
The MySQL database was backed up using the mysqldump utility. This creates a logical backup of the schema and data.
Command:
mysqldump -u [username] -p [database_name] > database_backup.sql
Explanation:
● [username]:Replacewiththedatabaseusername.
● [database_name]:Replacewiththenameofthedatabasetobackup. ● database_backup.sql:Thefilewherethebackupwillbestored.
Step 2: Verify the Backup File
After creating the backup, the file was checked to ensure it contains the expected data.
Command:
less database_backup.sql
Recovery Process
Step 1: Restore a MySQL Database
   
 The backed-up data was restored into the MySQL database using the mysql command. Command:
mysql -u [username] -p [database_name] < database_backup.sql
Explanation:
● [username]:Replacewiththedatabaseusername.
● [database_name]:Replacewiththenameofthedatabasetorestoreinto. ● database_backup.sql:Thebackupfiletoberestored.
 Summary
Process Overview Step
Outcome
Database Backup
Backup Verification
Database Recovery
Successfully backed up using mysqldump.
Backup file verified for completeness. Successfully restored using mysql.
 Challenges Faced
File size for larger databases: Addressed by compressing the backup file. Command:
gzip database_backup.sql
● Compatibility issues during recovery: Resolved by ensuring both backup and recovery were performed on the same MySQL version.
Outcome
The backup and recovery processes were completed successfully. The database is now safeguarded against potential data loss scenarios.
  
Recommendations
Automate the backup process using cron jobs for periodic backups. Example Cron Job: 0 2 * * * mysqldump -u [username] -p[password] [database_name] >
/path/to/backup/database_backup_$(date +\%F).sql
1. Store backups in a secure, off-site location for additional redundancy.
2. Test recovery periodically to ensure the process works as expected

## Summary Report
<img width="986" alt="Screenshot 2025-01-11 at 9 04 38 PM" src="https://github.com/user-attachments/assets/5f675c02-ba64-4ffa-883e-2ef432a3ce6f" />

 
