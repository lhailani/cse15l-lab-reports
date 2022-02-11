# Lab Report 3: week 6

In this lab report, I will be showing how to streamline `ssh` configuration.

Originally, logging into `ieng6` you have to type your whole username. By using:

` $ ssh cs15lwi22atx@ieng6.ucsd.edu `

However, there is a another and shorter way to log into your `ssh` by giving yourself a nickname. 

This can be done by creating file named `config` within your `.ssh` folder. On visual studio code it should
look similar to this format. Additionally, you should also copy the following contents but use your own username. 

![image](https://user-images.githubusercontent.com/97707886/153661186-f2a2447b-0b27-41a0-b452-3df734eabbc9.png)

(*instead of ieng6 you can change to a different username*)

Once the file `config` is created and saved you can run in the terminal:
` $ ssh ieng6`  (*or whatever nickname you used*) 

Now running the `ssh` command using the new nickname, the terminal should look like the following:
![image](https://user-images.githubusercontent.com/97707886/153663452-e1061c83-6cc5-414f-8867-b0873b16abf6.png)

Furthermore, we can use `scp -r` to copy a whole directory. The command line should look like this with
your new nickname. 

`$ scp -r path ieng6.ucsd.edu:~/markdown-parse`

Though, `path` is the actual path of the directory on your computer. Running the command it should produce something similar
to this, depending on the amount of files within your directory:
![image](https://user-images.githubusercontent.com/97707886/153666014-6a129dd4-a35f-45c8-a899-0b9810dd72b6.png)














