# Lab Report 1: week 2

## Topic: remote access

Hello, this is a step-by-step tutorial on how to log into your course-specified account on ieng6! 
Here are the following steps I took to achieve this:

1) **Installing Visual Studio Code:**
- Go to the Visual Studio Code website: [Link](https://code.visualstudio.com/)
     - Follow the instructions and download the version for the platform you are working on (such as Windows or OSX)
- As a result, visual studio code should open and look like this:
<img src="https://user-images.githubusercontent.com/97707886/149439161-eb548d36-c96c-464e-8fa9-7788b737f059.png" width="700"          height="500">

2) **Remotely Connecting:**

- First, [Install OpenSSH](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse)
- Then, find your course specified account w/ the link: [Link](https://sdacs.ucsd.edu/~icc/index.php)
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
- `ls -lat`: lists hidden files
     - Remote computer (after ssh-ing):
          >![image](https://user-images.githubusercontent.com/97707886/149448669-91691db3-da81-4a93-a7b3-cd06e399e323.png)
     - My computer:
          >![image](https://user-images.githubusercontent.com/97707886/149448727-1cc0b7ea-ae58-44cc-839d-71b9d6dbf72d.png)
- `ls -a`: shows all the hidden files starting with "."
     - Remote computer (after ssh-ing):
          >![image](https://user-images.githubusercontent.com/97707886/149448788-5352e9ca-5d3f-4fb6-b1fb-0a82b0cc18d3.png)
     - My computer:
          >![image](https://user-images.githubusercontent.com/97707886/149448830-78cf5204-b061-455f-9a50-639ebfd71618.png)
- `ls <directory>` (`<directory>` is replaced with `/home/linux/ieng6/cs15lwi22/cs15lwi22abc` and `abc` should be replaced with your user : lists all files in current directory
     - Remote computer (after ssh-ing):
          >![image](https://user-images.githubusercontent.com/97707886/149448926-ae206166-e4f4-4961-8fdf-911011f4cd7c.png)
     - My computer:
          >![image](https://user-images.githubusercontent.com/97707886/149448971-2fbe4f83-31d8-4b95-bc1e-773c1ed9e043.png)  
- `cp /home/linux/ieng6/cs15lwi22/public/hello.txt ~/` : `cp` = copy 
     - Remote computer (after ssh-ing):
          >![image](https://user-images.githubusercontent.com/97707886/149449046-3f5eeaf3-60b3-4d0f-854a-56d7c558b7a8.png)
- `cat /home/linux/ieng6/cs15lwi22/public/hello.txt`
     - Remote computer (after ssh-ing):
          >![image](https://user-images.githubusercontent.com/97707886/149449149-6f4e1b6f-c05d-4aac-b3ca-03417d120323.png)

Furthermore, to log out of the remote server you can either type `exit` or run the command Ctrl-D

4) **Moving Files with scp**

To copy a file from a local computer to a remote computer, we use the command `scp`. 
Create a new file on your computer named `WhereAmI.java` and include the following contents:
> ![image](https://user-images.githubusercontent.com/97707886/149474154-461ff294-d487-49a6-9c86-78b13b662ff7.png)

Now, in the terminal from the directory the file was created, run the command but with your username:
> ![image](https://user-images.githubusercontent.com/97707886/149474647-09534ddb-92a5-4a09-90e0-8815eaeb1524.png)

You will be asked for your password and it would be the same as the one you used to log in with `ssh`.

To check if it is in you ieng6 directory, log in `ssh` and use the `ls` command. The terminal should look something like this:
> ![image](https://user-images.githubusercontent.com/97707886/149475178-78fc8e1e-916f-4003-b5b2-c11d0ad6d498.png)

5) **Setting an SSH key**

The `ssh` key allows you to `ssh` or `scp` withouth entering a password.

In order to do this, type in the terminal '$ ssh-keygen` and then the terminal should run like the following:
>![image](https://user-images.githubusercontent.com/97707886/149516896-f5640a0d-32cf-4740-9cb1-04fb202a2a2d.png)
- the overwrite question is not included yours if you haven't set one 

Additionally, window users would need to follow extra `ssh-add` steps: [Link](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_keymanagement#user-key-generation)
- example (since I had Windows I had to include `ssh-add`):
>![image](https://user-images.githubusercontent.com/97707886/149521804-e68dcc37-7171-4d5a-9580-769855a6b500.png)


Two new files have now been created which is the private key (`id-rsa`) and the public key (`id_rsa.pub`) ; both are stored in the `.ssh` directory on your computer. 

Then, the public key needs to be copied to the `.ssh` directory of your account onto the server. 

a) log into your account  `$ ssh cs15lwi22atx@ieng6.ucsd.edu`

b) once in the server run the following `mkdir .ssh`

c) then *logout*

d) on the client run the following `scp` command but with your file names: ![image](https://user-images.githubusercontent.com/97707886/149522450-5a3f49b8-3ede-48c2-be4a-20bd566ea7b8.png)

Now, you are able to access `ssh` and `scp` without always inserting your password!

6) **Optimize Remote Running**

There are many ways to optimize remote running which can improve efficiency and take less time or typing. 
For instance, one example is that you can use semicolons to run commands on the same line within the terminal. 

Try the following: 
`$ cp WhereAmI.java OtherMain.java; javac OtherMain.java; java WhereAmI`

The terminal should look alike with this:
> ![image](https://user-images.githubusercontent.com/97707886/149587529-a98653bc-3a99-4887-8c0e-9adf076743d1.png)

Additionally, there are many more commands to try out which could be quicker and take less time to type it one by one. 

Overall, these are the basic steps on how to remote access from your local computer! 

----












