# Lab Report 1: week 2

## Topic: remote access

Hello, this is a step-by-step tutorial on how to log into your course-specified account on ieng6! 
Here are the following steps I took to achieve this:

1) **Installing Visual Studio Code:**

     - Go to the Visual Studio Code website: [Link](https://code.visualstudio.com/)
        - Follow the instructions and download the version for the paltform you are woking on (such as Windows or OSX)
     - As a result, visual studio code should open and look like this:
        <img src="https://user-images.githubusercontent.com/97707886/149439161-eb548d36-c96c-464e-8fa9-7788b737f059.png" width="700"          height="500">

2) **Remotely Connecting:**
    - First, [Install OpenSSH](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse)
    - Then, find your course specified account: [Link](https://sdacs.ucsd.edu/~icc/index.php)
    - Now open a terminal in Visual Studio Code (which can be done by clicking *Terminal* &#8594; *New Terminal* or doing the command Ctrl + Shift + ` )
       - Type into the Terminal: `$ ssh cs15lwi22atx@ieng6.ucsd.edu`
          -  However, *cs15lwi22atx* should be replaced with your course specific number
       - If it is your first time connecting you wil be asked a question if you want to continue connecting.  So, type `yes` and then          you will be prompted to type in your account password.
          - You will not be able to see your password when typing it out but make sure it is being typed correctly
       - Once those steps have been completed, the terminal should look similar to this:
         ![image](https://user-images.githubusercontent.com/97707886/149441581-328b7ec8-a745-482f-b161-0a748b81b854.png)
        
3) **Tring Some Commands**
