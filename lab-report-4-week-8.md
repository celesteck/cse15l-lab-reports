# Lab Report 4, Week 8
- In order to identify the **correct** output of each snippet, I used [Commonmark](https://spec.commonmark.org/dingus/?text=%60%5Ba%20link%60%5D(url.com)%0A%0A%5Banother%20link%5D(%60google.com)%60%0A%0A%5B%60cod%5Be%60%5D(google.com)%0A%0A%5B%60code%5D%60%5D(ucsd.edu)%0A%0A)
- Link to [my-markdown-parse](https://github.com/celesteck/markdown-parser-new)
- Link to [markdown-parse-week7](https://github.com/ima-quack/markdown-parser)
***
### **Snippet 1**

This should produce [`google.com, google.com, ucsd.edu]

- In order to test this case, I did:
- ![image](https://user-images.githubusercontent.com/100736576/169719211-7be7f259-41d1-4cb3-a647-70a014fc2ba8.png)

-However, this is what error we get when we run a junit test on my implementation:
- it `**FAILED**`
![image](https://user-images.githubusercontent.com/100736576/169719583-e9a11299-105a-4e43-9b3e-220bc1d87a6a.png)
1. In order to fix make my program produce the correct output, I think that it would take less than 10 lines of code. I could simply add an if statement to check for characters that preceed the `opening bracket` character, specifically for the " ` " character. If it is there, it will go to the next opening bracket and not return this link. 

-This is what we get when we run a junit test on the *other* implementation:
- it `**FAILED**`
![image](https://user-images.githubusercontent.com/100736576/169719596-17ec4a88-c1c5-40fc-9815-81bb5785498a.png)

***

### **Snippet 2**

The expected output should be [a.com, a.com(()), example.com]
- In order to test this case, I did:
- ![image](https://user-images.githubusercontent.com/100736576/169719280-cc946850-f16a-46c3-8f7e-de93dba71ae4.png)

-This is what happens when the test is run on my implementation:
- it `**FAILED**`
![image](https://user-images.githubusercontent.com/100736576/169719659-21b26bb3-617e-4cf9-a043-b9a1300ed27e.png)
1. For this implementation, I realized that I failed to account for the nested links. I think that in this case, I could create an if statement to check if the **index of** the `open bracket` is less than than the **index of** the `close bracket` from the previous open bracket. If it is, then it will read that link. I think that this case would be less than 10 lines of code.

-Here is the output from the *other* implementation:
- it `**FAILED**`
![image](https://user-images.githubusercontent.com/100736576/169719638-d3f0fe62-a343-4374-a5e7-dc94e1f19160.png)


***

### **Snippet 3**

The expected output should be [https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule]

- In order to test this case, I did:
- ![image](https://user-images.githubusercontent.com/100736576/169719298-82a705c9-a545-467d-b0ea-dc2fc143ac7d.png)


-This is the result of the junit test on my implementation: 
- it `**FAILED**`
![image](https://user-images.githubusercontent.com/100736576/169719680-ed366625-ef5f-4587-abd3-7d4b2821a413.png)
1. My program for this case fails because it does not account for all of the `extra space` that is left between all of `()` and `[]`. In order to fix this case, I think that it might be possible to solve this in less than 10 lines. If I create an if statement that checks what the character **following** the `open bracket` or `open parenthesis` is. If it is an `open space` " ", then it will not return the link within the parenthesis. 
-This is the result from the *other* implementation:
- it `**FAILED**`
![image](https://user-images.githubusercontent.com/100736576/169719693-53ca3ef3-729d-48d7-9452-0b1a51211bbf.png)
