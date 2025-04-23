# Log Analysis in Linux and Splunk

In this lab project, I will analysis on logs I could search and find through Kali Linux and Splunk. Lab practice apart of Infosec Learning and through Springboard Curriculum. 

Linux Analysis

1. Sign and log into your Kali Linux VM.

2. From here I am going to confirm and find out the version I am running through the terminal.

- Type in the command: uname -a

3. Once it is confirmed, I will pull up a list of all of the files and folders within the root directory.

- Type in the command: ls

4. From here I found a log within the root directory.

<img width="631" alt="image" src="https://github.com/user-attachments/assets/add474c5-8967-4276-9441-b973dc3c2d5e" />

The results from steps 2, 3, and 4

5. After identifying the log, I want to view the log files to do so I will type in the following command

- Type in the command: cat ex191112.log

<img width="437" alt="image" src="https://github.com/user-attachments/assets/219b3eaf-352f-4976-ad26-dd499bdedf12" />

The result of step 5

6. The log file contains many lines and can be hard to understand the amount that there is to this file.

7. I will use the wc command, wc a program used to display the line, word, character, and byte count of a file.

- Type in the command: wc --help

8. Things that you are able to do with wc command:

Type in the following commands for the these results:

- wc -l file.log: View the number of lines in the file.

- wc -c file.log: View the number of bytes in the file.

- wc -m file.log: View the number of characters in the file.

- wc -w file.log: View the number of words in the file.

<img width="568" alt="image" src="https://github.com/user-attachments/assets/256c3e5f-5577-43cd-98bb-f3340f449d87" />

The results of step 8

9. The head command can be used to display the beginning or first lines of a file.

- Type in the command: head --help 

10. Now the same for the log. This will generate the first 10 lines of the log file.

- Type in the command: head ex191112.log

<img width="384" alt="image" src="https://github.com/user-attachments/assets/a1b46db3-8989-42b2-9ace-a0b997196199" />

The results of step 10 and 11

11. The tail command can be used to display the ending or last lines of a file.

- Type in the command: tail ex191112.log

<img width="380" alt="image" src="https://github.com/user-attachments/assets/e774ef4e-15fe-44da-a8da-a70483339011" />

12. To specify the number of lines from either the beginning or end of a file is to type the following:

- Type in the command: head -n (input number) log.file

- Type in the command: tail -n (input number) log.file

<img width="438" alt="image" src="https://github.com/user-attachments/assets/24d06242-a401-4240-9db6-27b51890f893" />

The results of step 12

13. 
