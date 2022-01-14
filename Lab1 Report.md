# CSE Lab1 Report

## <strong>Step 1: Install VS Code</strong><br/>
  To install VS Code, please visit https://code.visualstudio.com/ and select your platform. VS Code support major platforms such as Windows, macOS, and Linux.  
  
![Image](https://github.com/TSLAX/CSE15L-Lab/blob/main/images/Snipaste_2022-01-13_02-02-07.png)  
This page usually will automatically identify your platform, just simply click download Stable Build and install it on your computer as usual.  
  

## <strong>Step 2: Remotely Connecting</strong><br/>
University provides specific course accounts for students. For this step, we'll use a command which calls <strong>ssh</strong>  

For Windows:  
Before we get started, you need to install OpenSSH to connect your server or other computers. To install OpenSSH, please visit [Microsoft Documentation website](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse) and following this instruction to install it.  
  
  For macOS/Linux:  
  Since these operate system is Unix based operating systems, they have ssh integration built in, so you don't need to do any extra steps.  
  
  Check your own course-specific account for CSE15L：  
  [Click me to get your account](https://sdacs.ucsd.edu/~icc/index.php)  

  First, open your terminal in VS Code and input a command like this then replace the Mosaic part by the letters with your own account.  
  ![Image](https://github.com/TSLAX/CSE15L-Lab/blob/main/images/Snipaste_2022-01-13_02-39-09.png)  
  ![Image](https://github.com/TSLAX/CSE15L-Lab/blob/main/images/Snipaste_2022-01-13_02-42-39.png)  
  Input your password and logged in you will see something like this:  
  ![Image](https://github.com/TSLAX/CSE15L-Lab/blob/main/images/Snipaste_2022-01-13_03-06-18.png)  
  Now, you have successfully connected to your remote server.  
    
## <strong>Step 3: Trying Some Commands</strong><br/>  
Let's try to run some useful commands.  
<strong>ls</strong>: Lists all files and directories in the present working directory  
![alt test](https://github.com/TSLAX/CSE15L-Lab/blob/main/images/ls.png)  
  
<strong>ls - a</strong>: Lists hidden files as well  
![alt test](https://github.com/TSLAX/CSE15L-Lab/blob/main/images/ls-a.png)  
  

<strong>ls -lat</strong>: List files or directories in a table format with extra information including hidden files or directories:  
![alt test](https://github.com/TSLAX/CSE15L-Lab/blob/main/images/ls-lat.png)  
## <strong>Step 4: Moving Files with scp</strong><br/>  
Alright, since we're able to remote connect the server. Now. it's a good time to learn how to copy files to the server with scp.  
Step 1: Change the directory to the file location on the terminal that you want to copy to the server.  

cd /your/file/directory  
Step 2: Use the follow command to copy your file to the server.  
scp WhereAmI.java cs15lwi22zz@ieng6.ucsd.edu:~/  
Then, you'll be required to prompted password as usual.  
![Image]()