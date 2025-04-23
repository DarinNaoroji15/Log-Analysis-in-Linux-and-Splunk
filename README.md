# Log Analysis in Linux and Splunk

In this lab project, I will analysis on logs I could search and find through Kali Linux and Splunk.

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

8. 
