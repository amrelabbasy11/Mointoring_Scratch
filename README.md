# Monitoring_Script

This is a bash script that monitors system resources including disk usage, CPU usage, memory usage, and running processes. It logs the system status to a log file and sends notifications if certain thresholds are exceeded (e.g., disk usage over 80%).

### Requirements
The script performs the following tasks:
1. Check Disk Usage:
   - Report the percentage of disk space used for each mounted partition.
   - Warn if usage exceeds 80%.
   
2. Check CPU Usage:
   - Display the current CPU usage as a percentage.

3. Check Memory Usage:
   - Show total, used, and free memory.

4. Check Running Processes:
   - Display the top 5 memory-consuming processes.

5. *Generate a Report:*
   - Save the collected information into a log file (e.g., monitoring_scratch_infs.log).

----------------------------------------------------------------------------------------

## Script Details

The script works as follows:

- Disk Usage:
  - It uses the df -h command to check disk usage and triggers an email notification if usage exceeds 80%.

- CPU Usage:
  - It uses the top command to check the CPU usage percentage.

- Memory Usage:
  - It uses the free -h command to display total, used, and free memory.

- Running Processes:
  - It uses ps -eo pid,user,%mem,comm to display the top 5 memory-consuming processes.

- Logging:
  - The output of these commands is logged in the file /var/log/monitoring_scratch_infs.log.

----------------------------------------------------------------------------------------

## Prerequisites

Before running the script, ensure that the following tools are available:

- df
- top
- free
- ps
- mail (for sending email notifications)

You can install these tools using the package manager for your distribution (e.g., apt for Ubuntu or yum for CentOS).

----------------------------------------------------------------------------------------
## connect VM with github account

1. Set up your Git user name and email (these will be associated with your commits):
2. Generate SSH Key from your VM
3. Past public key ot SSH key
4. Test the Connection :Verify that your VM can connect to GitHub:
ssh -T git@github.com
----------------------------------------------------------------------------------------
## Creating Repo
1. Create repository on github
2. clone it to the local server using : git clone (link)
3. open scratch file in the cloned location
4. git add (name of scrtach file)
5. git commit -m " text"
6. push it to remote server

## CronJob to automate the script file 
![Cron_File](https://github.com/user-attachments/assets/26c2cad7-e27a-4c4f-9d71-e291d64a5f58)

## Mail image ![1000089824](https://github.com/user-attachments/assets/61676cc4-02e1-475a-8088-8caf357fc7b5)

## Sctipt output 
![1000089825](https://github.com/user-attachments/assets/3755e457-6f6d-40c1-b172-b816ae073f3f)

