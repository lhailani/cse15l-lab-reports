# Lab Report 5: week 10

In this lab, I will showcase two test where my group implementation had different answers than the implementation that was provided in lab 9.

**Explanation**
*How you found the tests with different results (Did you use diff on the results of running a bash for loop? Did you search through manually? Did you use some other programmatic idea?)*
- To find the tests with different results, I used the `diff` command: 
> ` $ diff markdownparse2/myresults.txt markdownparse1/results.txt`


For each test:
Describe which implementation is correct, or if you think neither is correct, by showing both actual outputs and indicating what the expected output is.
For the implementation that’s not correct (or choose one if both are incorrect), describe the _bug (the problem in the code). You don’t have to provide a fix, but you should be specific about what is wrong with the program, and show the code that should be fixed.


## Test 1: test-files/22.md

**Preview**:

![image](https://user-images.githubusercontent.com/97707886/157983911-f1b515cf-618c-48ee-829c-c40f1819eb63.png)

**Differences**:

![image](https://user-images.githubusercontent.com/97707886/157990540-201f2dd6-9e45-479f-8fce-23004eeff759.png)
> (*top result is the my markdownparse and bottom result is the class markdown parse*)

**Explanation**

Technically, my file was correct as it produced a link like the expected/preview. However, my program is incorrect because it is not a valid link. In this case, I will go further in depth how to address the issue in my Markdown-parse. We're getting the specific output from our Markdown-parse is because of how our while loop is formatted. Hence, is why we are getting a link in return. 
> ![image](https://user-images.githubusercontent.com/97707886/157987594-461b0796-5896-4491-97cc-d3c5de2f2be0.png)

To fix this, we can include things like an if statement that takes into consideration of other symbols that are not in a valid link. If those things occur, then the while loop breaks and no links should be returned.

## Test 2: test-files/577.md

**Preview**:
![image](https://user-images.githubusercontent.com/97707886/157989627-e2bddc37-7794-49f7-a9bb-1a513960f228.png)

**Differences**:

![image](https://user-images.githubusercontent.com/97707886/157989350-7bb827db-fa7b-4087-ac89-74ae3ca8b03e.png)
> (*top result is my markdownparse and bottom result is the class markdownparse*)

**Explanation**:

The preview indicates that an image link would be returned, though, it is not an actual image link. So, the image link should still be invalid and an empty list 
should be returned. My results is proven to be correct while the professors is incorrect. To address the professor's error we can consider not implementing an image link in the program, like how my group did in our Markdownparse. The professor's program does not take into consideration about image links which is why we get the results.

> ![image](https://user-images.githubusercontent.com/97707886/157993580-5edd0be2-1c5a-4107-b5a8-aa326652c7d7.png)

To implement that idea, we can include an if statement, if an "!" is at index 0, we break from the while loop and an empty list is returned. However, if we were to take into consideration about image links, we can still have the if statement but instead of breaking we would check if it's a valid image link. 


________


