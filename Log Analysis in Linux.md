# Log Analysis in Linux and Command Line Usage

In this lab project, I will analysis on logs I could search and find through Kali Linux.

Linux Analysis

1. Sign and log into your Kali Linux VM.

2. From here I am going to confirm and find out the version I am running through the terminal.

- Type in the command: uname -a

3. Once it is confirmed, I will pull up a list of all of the files and folders within the root directory.

- Type in the command: ls

4. From here I found a log within the root directory.

<img width="631" alt="image" src="https://github.com/user-attachments/assets/add474c5-8967-4276-9441-b973dc3c2d5e" />

Results from steps 2, 3, and 4

5. After identifying the log, I want to view the log files to do so I will type in the following command

- Type in the command: cat file.log

<img width="437" alt="image" src="https://github.com/user-attachments/assets/219b3eaf-352f-4976-ad26-dd499bdedf12" />

Result of step 5

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

Results of step 8

9. The head command can be used to display the beginning or first lines of a file.

- Type in the command: head --help 

10. Now the same for the log. This will generate the first 10 lines of the log file.

- Type in the command: head file.log

<img width="384" alt="image" src="https://github.com/user-attachments/assets/a1b46db3-8989-42b2-9ace-a0b997196199" />

Results of step 10 and 11

11. The tail command can be used to display the ending or last lines of a file.

- Type in the command: tail file.log

<img width="380" alt="image" src="https://github.com/user-attachments/assets/e774ef4e-15fe-44da-a8da-a70483339011" />

12. To specify the number of lines from either the beginning or end of a file is to type the following:

- Type in the command: head -n (input number of your choice) log.file

- Type in the command: tail -n (input number of your choice) log.file

<img width="438" alt="image" src="https://github.com/user-attachments/assets/24d06242-a401-4240-9db6-27b51890f893" />

Results of step 12

13. The grep command is used to parse for certain terms or expressions within a file.

- Type in the command: grep --help

14. To view the key words or anything that occurs in the log file.

- Type in the command: cat file.log | grep (input keyword of your choice)

* It is important to ensure proper pronuciation or spelling is used or no results will generate.

<img width="452" alt="image" src="https://github.com/user-attachments/assets/07625688-cd58-4240-8424-0354761696c1" />

Results of step 14

15. Leafpad is an open-source and useful text editor tool in Linux. By using the Leafpad command you can edit or change text within the original log file.

- Type in the command: leafpad file.log

<img width="520" alt="image" src="https://github.com/user-attachments/assets/d22df8fe-d424-4e95-9e43-90aeb685f8fd" />

Result from step 15

16. From here you can choose to delete or edit any lines to the log file. After completing any edits, you can save and close the file.

17. The gawk command is a powerful program you can use to find pattern-matching/processing language.

- Type in the command: gawk --help

18. To display the first column or any columns type the following:

- Type in the command: cat file.log | gawk '{print $1}'

<img width="388" alt="image" src="https://github.com/user-attachments/assets/adc68766-7455-4056-8308-59fa0e6ea0d7" />

Results from step 18

19. The sort command can help put and order the columns a log file.

- Type in the command: sort --help

20. The uniq command can show all the output in unique way.

- Type in the command: uniq --help

21. If you combine both sort and uniq you can display unique values within each column or section of the file. This command will show unique values from the first command for example.

- Type in the command: cat file.log | gawk ‘{print $1}’ | sort | uniq -c

![image](https://github.com/user-attachments/assets/b68df400-aae3-4133-880b-a56d12fc44bd)

Result from step 21

My takeaway: Log files can be extremely large. A helpful way to view the output of the log file is by using the command line in Linux. The commands used below can help with this process. Typing in the --help command will "help" and give you full context on which syntax to use, when trying to specify your parameters.

- The cat command in Linux will allow you to view a file.

- The grep command can be used to parse through the information.

- The head command will show you the first lines in a file.

- The tail command will show you the last few lines.

- Using a combination of the gawk, sort, and uniq commands, you can find out specific information about events in log files.
