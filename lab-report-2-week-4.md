# Lab Report 2: week 4

In this lab report, I will be discussing 3 code changes that me and my peers have done in our recent labs to improve our program. 

**1. Improving our program part 1:**

In this case, we tried a file that used only `()` but not `[]`.

First, we created a file that shouldn't work:[Failed File 1](https://github.com/lhailani/markdown-parse/blob/main/md3.md).

In the terminal, running the program: 

![image](https://user-images.githubusercontent.com/97707886/151602597-5c825b69-db96-4baf-802e-9be1757b4ed4.png)

Our code changes: ![image](https://user-images.githubusercontent.com/97707886/151602186-dadf4178-26ca-40dc-8e3c-440a12a08eea.png)

The bug in our code was that it was reading the file when it shouldn't because the test file was written incorrectly. Which was caused because the program files were reading things at a certain index, producing an output that we did not want/expect. Fixed this by adding an `if` statement to limit this and the program should return `[]`. 

**2. Improving our program part 2:**

Another test we tried, was using a file that only use `[]` but not `()`.

A file that should not work: [Failed File 2](https://github.com/lhailani/markdown-parse/blob/main/newmarkdown.md)

In the terminal, running the program produced an error message:![image](https://user-images.githubusercontent.com/97707886/151605463-a33c2674-1cf1-4b09-868d-111f4b9a5619.png)

Our code changes: ![image](https://user-images.githubusercontent.com/97707886/151605766-3cee310d-2025-4a2b-9893-1b2c3bbf3093.png)

The bug in our code was that there was an index out of bound message because of our file. The previous correction we have done from part 1 took into consideration of files without `[]`, however, not files without `()`. Those correction affected how the file was read and we got an index out of bound. Fixed this by adding more to the if statement. 

**3. Improving our program part 3:**

The last test file we created, was using a file that had a `[]` and `()`, very apart from one another.

File that should not work: 

[Failed File 3](https://github.com/lhailani/markdown-parse/blob/main/md4.md)

In the terminal, running the program returns:

![image](https://user-images.githubusercontent.com/97707886/151610271-caa154f3-de4a-4282-a5aa-554caca46127.png)

Our code changes:

![image](https://user-images.githubusercontent.com/97707886/151610517-1fcc749c-c872-4d39-8b81-a25a9de6ee5f.png)



