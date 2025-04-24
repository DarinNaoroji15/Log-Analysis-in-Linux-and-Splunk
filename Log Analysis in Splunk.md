# Log Analysis in Splunk

1. Log into your Windows 10 VM.

2. Open and run your Splunk enivronment.

3. Click on Explore Splunk on the top right of the window.

![image](https://github.com/user-attachments/assets/e07aed0e-3cd7-49b4-817c-a61a0290017c)

Result from step 3

4. Click Add Data.

![image](https://github.com/user-attachments/assets/c492afcd-10f8-4498-997b-2c3bbfc7c93e)

Result from step 4

5. Click upload files from my computer.

![image](https://github.com/user-attachments/assets/06de4224-3613-43ff-8c2e-a58ce8e09bfa)

Result from step 5

6. Click Select File.

![image](https://github.com/user-attachments/assets/41472e5a-8468-4b42-8cde-a9159c84505f)

Result from step 6

7. From the File Directory navigate to This PC -> Desktop -> files folder -> Select file.log

![image](https://github.com/user-attachments/assets/45b707c4-4aaf-4d07-948d-33e470d315be)

Result from step 7

8. Click Next on Splunk.

9. For this example, we will ensure the Source Type is iis. The source type is the type of log file that Splunk is going to analyze. iis is a web server on Windows web servers.

10. Click Next on Splunk.

![image](https://github.com/user-attachments/assets/0773db45-2177-4c5f-b908-534a955b61f2)

Results from step 9 and 10

11. Click Review on Splunk.

![image](https://github.com/user-attachments/assets/cf4290b3-44e1-4309-82c6-b83585de734b)

Result from step 11

12. Click on Submit on Splunk.

![image](https://github.com/user-attachments/assets/7a7575b2-643e-4363-9549-303494dffdc3)

Result from step 12

13. Click Start Searching on Splunk.

![image](https://github.com/user-attachments/assets/adcb5661-14ce-4d2c-8eeb-79515db928ae)

Result from step 13

14. Search and type in 530. The "530" event code in IIS is a User cannot login error.

![image](https://github.com/user-attachments/assets/cb7a7ebc-3820-4453-8ccf-3ce2a1cd85e9)

Result from step 14

15. This is same number that the number of events with the code of 530 is 180,855. This was the exact same number of these event codes when we used all of the Linux commands below to parse the information.

root@kali:~# cat file.log | gawk ‘{print $5}’ | sort | uniq -c

16. Search and type in 230. The "230" is a sucessful log event code in IIS.

![image](https://github.com/user-attachments/assets/44abb7c7-2bcb-4312-bcf7-972c6979251b)

Result from step 16

17. This is same number the number of events with the code of 230 is 2. This was the exact same number of these event codes when we used all of the Linux commands below to parse the information.

root@kali:~# cat file.log | gawk ‘{print $5}’ | sort | uniq -c
