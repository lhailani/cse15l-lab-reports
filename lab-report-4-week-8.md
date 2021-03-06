# Lab Report 4: week 8

Links to markdown-parse repository 
- [my markdown-parse](https://github.com/lhailani/markdown-parse)
- [peer reviewed markdown-parse](https://github.com/Darrengn/markdown-parse)


### Snippet 1:
![image](https://user-images.githubusercontent.com/97707886/155748447-50f0ea16-8f4f-4259-9e83-719f0e11db5d.png)
### Snippet 2:
![image](https://user-images.githubusercontent.com/97707886/155748695-90b8e784-b2b5-48e0-8afb-f172a50f209d.png)
### Snippet 3:
![image](https://user-images.githubusercontent.com/97707886/155749236-ecf4425c-f385-487f-9545-a521382600e3.png)

### How test cases were written: 
![image](https://user-images.githubusercontent.com/97707886/155799807-a3452fc2-fc39-43a5-b4b7-ace985d25385.png)

### My implementation output:
![image](https://user-images.githubusercontent.com/97707886/155800400-01849024-afaf-4f57-b16f-45b12f374ed6.png)

### Reviewed markdown-parse implementation output:
![image](https://user-images.githubusercontent.com/97707886/155801087-e7604d19-3c33-440c-8ee3-6d42c053a3f7.png)

## Questions

**Do you think there is a small (<10 lines) code change that will make your program work for snippet 1 and all related cases that use inline code with backticks? If yes, describe the code change. If not, describe why it would be a more involved change.**

- For snippet 1, I don't think there would be much line changes within our code. For instance, we could add another if statement that looks for the criteria of backticks. 

**Do you think there is a small (<10 lines) code change that will make your program work for snippet 2 and all related cases that nest parentheses, brackets, and escaped brackets? If yes, describe the code change. If not, describe why it would be a more involved change.**

- No, I think there would be more changes involves for our program to work. As snippet 2, takes into consideration of nested parentheses, brackets, and escaped brackets. We would have to write additional lines of code (most likely >10 lines) that considers these special factors. Our current program only checks for open and closed parentheses/brackets. Also, checks for spaces between lines. However, it does not check the special cases within snippet 2, so, multiple lines of code would be needed to check for these cases. Furthermore, there would be other special cases that snippet 2 does not cover. 

**Do you think there is a small (<10 lines) code change that will make your program work for snippet 3 and all related cases that have newlines in brackets and parentheses? If yes, describe the code change. If not, describe why it would be a more involved change.**

- More changes would definitely be needed to address the special cases in snippet 3. As the output, included links that were not expected. Issues that we would need to address and include in our program would be looking for spaces *in* brackets and the parentheses. Also, taking into consideration random lines of text that are not links. There are a lot of special cases that our program did not cover and would take more than 10 lines of code. We would also have to think of other related cases too.

