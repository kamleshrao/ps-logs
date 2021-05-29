# Setup Batch File for Logging your Internet Connection Network Issues 

1. Create folders as shown below:
```
c:\utils
c:\utils\scripts 
c:\utils\logs 
```
2. Create act-ping-loop.bat file to c:\utils\scripts. Update its contents with the code given in the below next section.
3. (Optional) - In case if you are using D: or any other drive, edit the [act-ping-loop.bat] file and change the drive letter in line#5
4. Goto command prompt and change directory to c:\utils\scripts.
5. Type act-ping-loop.bat to run the batch file.
6. The log file will be created in C:\Utils\Logs folder. 


## Contents of ```act-ping-loop.bat```
```
@ECHO OFF
ECHO Recording Internet Ping Result.  Press CTRL+C to stop!
:START
SET CUR_DATE=%date:~6,4%%date:~3,2%%date:~0,2%
SET FILENAME="c:\utils\logs\act-ping-loop-log-%CUR_DATE%.txt"
ECHO [Timestamp] %date% %time% >> %FILENAME% 
PING www.google.com >> %FILENAME% 
ECHO. >> %FILENAME% 
GOTO START

```
