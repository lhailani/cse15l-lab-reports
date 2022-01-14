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
        
3) **Trying Some Commands**
Now, we will attempt to run a few programs remotely after ssh-ing and also trying them on our local computer. 
The following commands we will type in the terminal:
- `cd ~`:goes to home directory 
- `cd`: changes directory
- `ls -lat`
     - Remote computer (after ssh-ing):
          >![image](https://user-images.githubusercontent.com/97707886/149448669-91691db3-da81-4a93-a7b3-cd06e399e323.png)
     - My computer:
          >![image](https://user-images.githubusercontent.com/97707886/149448727-1cc0b7ea-ae58-44cc-839d-71b9d6dbf72d.png)
- `ls -a`: 
     - Remote computer (after ssh-ing):
          >![image](https://user-images.githubusercontent.com/97707886/149448788-5352e9ca-5d3f-4fb6-b1fb-0a82b0cc18d3.png)
     - My computer:
          >![image](https://user-images.githubusercontent.com/97707886/149448830-78cf5204-b061-455f-9a50-639ebfd71618.png)
- `ls <directory>` (`<directory>` is replaced with `/home/linux/ieng6/cs15lwi22/cs15lwi22abc` and `abc` should be replaced with your user
     - Remote computer (after ssh-ing):
          >![image](https://user-images.githubusercontent.com/97707886/149448926-ae206166-e4f4-4961-8fdf-911011f4cd7c.png)
     - My computer:
          >![image](https://user-images.githubusercontent.com/97707886/149448971-2fbe4f83-31d8-4b95-bc1e-773c1ed9e043.png)  
- `cp /home/linux/ieng6/cs15lwi22/public/hello.txt ~/`
     - Remote computer (after ssh-ing):
          >![image](https://user-images.githubusercontent.com/97707886/149449046-3f5eeaf3-60b3-4d0f-854a-56d7c558b7a8.png)
     - My computer:
          >![image](https://user-images.githubusercontent.com/97707886/149449085-7090acf1-efc7-4453-acf5-bd6f07778ee7.png) 
- `cat /home/linux/ieng6/cs15lwi22/public/hello.txt`
     - Remote computer (after ssh-ing):
          >![image](https://user-images.githubusercontent.com/97707886/149449149-6f4e1b6f-c05d-4aac-b3ca-03417d120323.png)
     - My computer:
          >![image](https://user-images.githubusercontent.com/97707886/149449176-5e6d14fd-ac5b-4ff2-9cb9-4f4c4b92f4da.png)

