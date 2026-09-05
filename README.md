# Windows-basic-commands-batchscript
Ex08-Windows-basic-commands-batchscript

# AIM:
To execute Windows basic commands and batch scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware 

### Step 2:

Write the Windows commands / batch file . Save each script in a file with a .bat extension. Ensure you have the necessary permissions to perform the operations. Adapt paths as needed based on your system configuration.
### Step 3:

Execute the necessary commands/batch file for the desired output. 




# WINDOWS COMMANDS:
## Exercise 1: Basic Directory and File Operations
Create a directory named "my-folder"

## COMMAND AND OUTPUT

```

mkdir my-folder


```

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f4173843-7e14-4227-939e-b7fba1150d2f" />


Remove the directory "my-folder"

## COMMAND AND OUTPUT

```

rmdir my-folder


```

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/6e0f7030-580e-4e77-899a-d3c9f3362bfe" />



Create the file Rose.txt

## COMMAND AND OUTPUT

```

copy con Rose.txt

then enter:

A clock in a office can never get stolen
Too many employees watch it all the time

````


<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/25315326-ccd2-4b77-9a47-db5cf23b621e" />


Create the file hello.txt using echo and redirection

## COMMAND AND OUTPUT

```

echo "hello world" > hello.txt


```

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/d9a4b287-2ce4-4389-93dc-69586dccbbd7" />


Copy the file hello.txt into the file hello1.txt

## COMMAND AND OUTPUT

```
copy hello.txt hello1.txt

```

<img width="1036" height="297" alt="image" src="https://github.com/user-attachments/assets/6ec741e4-743e-4c5d-a918-3010a95137e9" />



Remove the file hello1.txt

## COMMAND AND OUTPUT

```
del hello1.txt

```
<img width="1092" height="262" alt="image" src="https://github.com/user-attachments/assets/8f3b045a-30c4-485f-bf9e-0301142e6c12" />


List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT

```

dir hello1.txt


```

<img width="990" height="237" alt="image" src="https://github.com/user-attachments/assets/ea7407b0-1557-4969-bd55-03f3502ac818" />



List out all the associated file extensions 

## COMMAND AND OUTPUT

```

assoc | more

```
<img width="1242" height="945" alt="image" src="https://github.com/user-attachments/assets/0239ef03-baf3-4de9-9e02-2ebcf6d914ae" />



Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT

```
fc hello.txt Rose.txt

```




## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".

```

1.bat

CODE :

@echo off
set name=John
echo Hello, %name%!
pause

```

## OUTPUT


<img width="1452" height="613" alt="image" src="https://github.com/user-attachments/assets/d7bb0c8d-5122-4b36-816e-988d66c571bc" />



2. Batch file to check whether a number is odd


Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.

Create:

2.bat

```

code :

@echo off
:main
set /p number=Enter a number:
rem Calculate remainder when divided by 2
set /a remainder=%number% %% 2
if %remainder%==1 (
 echo %number% is an odd number.
) else (
 echo %number% is not an odd number.
)
:choice
set /p continue=Do you want to check another number? (Y/N):
if /i "%continue%"=="Y" goto main
if /i "%continue%"=="N" goto end
echo Invalid choice, please enter Y or N.
goto choice
:end
echo Thank you for using the odd number checker!
pause


```

## OUTPUT

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/81e8b98f-7502-4613-81f6-26293ef60364" />





Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.

```
3.bat


code:
@echo off
for %%i in (1 2 3 4 5) do (
 echo Number: %%i
)
pause

```

## OUTPUT




<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/d954e1dc-c750-49f5-b944-49f77f5bc88e" />



Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):

```
code:

@echo off
if exist sample.txt (
 echo sample.txt exists.
) else (
 echo sample.txt does not exist.
)
pause

```

![Uploading image.png…]()



## OUTPUT
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/84322fb5-3239-41b4-96b6-efaa8829e8ac" />


Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.


## OUTPUT
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/ed06efad-b92c-4cb3-8963-54e2b913e0af" />



# RESULT:
The commands/batch files are executed successfully.

