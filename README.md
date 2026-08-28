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

Remove the directory "my-folder"

## COMMAND AND OUTPUT

<img width="1061" height="182" alt="image" src="https://github.com/user-attachments/assets/0b53d9c3-a0b1-45cf-900e-8992a45de40b" />

Create the file Rose.txt

## COMMAND AND OUTPUT
<img width="1147" height="427" alt="image" src="https://github.com/user-attachments/assets/b406b897-5a5c-4598-a7c8-fe0960870412" />


Create the file hello.txt using echo and redirection

## COMMAND AND OUTPUT
<img width="1143" height="433" alt="image" src="https://github.com/user-attachments/assets/521387e8-feed-4c13-9aa5-853acf925a16" />

Copy the file hello.txt into the file hello1.txt

## COMMAND AND OUTPUT
<img width="1117" height="147" alt="image" src="https://github.com/user-attachments/assets/3ff7e447-b785-4716-8886-337a64485309" />

Remove the file hello1.txt

## COMMAND AND OUTPUT
<img width="1122" height="311" alt="image" src="https://github.com/user-attachments/assets/45327118-82d3-4ee4-b627-243439355c71" />

List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT
<img width="776" height="241" alt="image" src="https://github.com/user-attachments/assets/28bd33c2-6e0f-4687-af71-b3409c38d195" />

List out all the associated file extensions 

## COMMAND AND OUTPUT

<img width="1147" height="810" alt="image" src="https://github.com/user-attachments/assets/e4065762-3cfc-4ddb-9df2-0c1c50ad1863" />

Compare the file hello.txt and rose.txt
## COMMAND AND OUTPUT
<img width="977" height="285" alt="image" src="https://github.com/user-attachments/assets/a9f619de-5436-40b5-b3cd-ecc3b1b2da8e" />

## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".
```
@echo off
set name=John
echo Hello, %name%!
pause
```




## OUTPUT

<img width="822" height="117" alt="image" src="https://github.com/user-attachments/assets/b2aa44b3-2bc2-4387-95ed-dc45d1883560" />


Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.
```
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

<img width="1120" height="310" alt="image" src="https://github.com/user-attachments/assets/0c3226f3-ebed-4779-a704-e6bb1c0e4d60" />



Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.

```
@echo off
for %%i in (1 2 3 4 5) do (
    echo Number: %%i
)
pause
```


## OUTPUT

<img width="992" height="242" alt="image" src="https://github.com/user-attachments/assets/c6914070-4fc3-4a16-861a-557407751f86" />



Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):
```
@echo off
if exist sample.txt (
    echo sample.txt exists.
) else (
    echo sample.txt does not exist.
)
pause
```
## OUTPUT
<img width="981" height="282" alt="image" src="https://github.com/user-attachments/assets/e3d44234-a079-48a8-9c84-1cd8b74002e5" />


Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.
```
@echo off
:menu
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
set /p choice=Choose an option: 
if "%choice%"=="1" goto hello
if "%choice%"=="2" goto createfile
if "%choice%"=="3" goto end

:hello
echo Hello, World!
goto menu

:createfile
echo Creating a file...
echo This is a new file > newfile.txt
goto menu
:end
echo Goodbye!
pause
```

## OUTPUT
<img width="963" height="566" alt="image" src="https://github.com/user-attachments/assets/9ea58fa4-d45f-46c0-a1cd-2454f5eb34e9" />



# RESULT:
The commands/batch files are executed successfully.

