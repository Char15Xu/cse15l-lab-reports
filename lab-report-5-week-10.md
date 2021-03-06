# Lab Report 5 Week 10
June 5th, 2022. Tianyang Xu. 

**Thank you to all the instructors in CSE15L!**

--- 

## Choose Test Cases
For this lab, the two tests I choose are 14 and 143 in the test-files directory.
I found the different results using vimdiff command in lab 9. 
![Image](lab5-1.png)

---

## Links
Here are the links for the two tests:
Test 14- [Link](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/14.md),
Test 143- [Link](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/143.md)

---

## Expected Output
For both tests, neither of my result was correct. For test 14, the expected output should be [], which has nothing inside. Also, test 143 should be [] with nothing inside since neither of these test cases has an actual link. The markdown-parse provided by the TA and my own markdown-parse both have incorrect output for test 14, but the TA does have the correct out put for test 143. To check, we can use VSCode preview.
For test 14, I get ![Image](lab5-14.png)
For test 143, I get ![Image](lab5-143.png)
Neither of these files have an actual link. 

---

## Actual Output
The expected output for both of these files is just no link at all. 
The actual output, however, is ![Image](lab5-actual1.png)

---

## Discussion
For test 14, the first problem is that the backslash escape disturbs the order of my program finding characters. Secondly, my markdown parse finds links based on looking for the open bracket, end bracket, open parentheses, and end parentese sequentially. The program will only stop if the count and currentIndex are less than the total length. If not, the program will keep finding brackets and parentheses in a sequence. With the backslash escape, this program reads the first three lines until count and currentIndex are less than the total length.

For test 143, the file is defining a function which is clearly not a link. The problem is that there is a parenthese which my program is looking for. It finds the x inside a pair of opening and closing parenthese and believed that it was the link. 

---

[Back to main page](https://char15xu.github.io/cse15l-lab-reports/)