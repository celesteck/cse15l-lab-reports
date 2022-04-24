# Lab Report 2
## CSE15L 4/22/2022

***

#### ***Code Change 1:***

*Fake link*

![image](https://user-images.githubusercontent.com/100736576/165000509-4c682f5a-8db8-495f-a798-b79dd3aa609f.png)

[Failure Inducing File](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-file8.md)


- When the proper format was followed, "[]()", but the content between the parenthesis was not a link, it would print out the content between the parenthesis. Since this was not a real link, it should have just returned "[]". In order to fix this, we used the "contains()" method to see if there was any empty space between the parethesis, if there was, that meant this was not a link and the loop should break and return nothing. 

***

#### ***Code Change 2:***

