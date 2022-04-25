# Lab Report 2
## CSE15L 4/22/2022

***

#### ***Code Change 1:***

*Fake link*

![image](https://user-images.githubusercontent.com/100736576/165001562-7467c50c-ca84-4f7e-92e7-0a51ce5ca8d4.png)


[Failure Inducing File](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-file8.md)

***Symptom***
`[a link on the first line]`


- When the proper format was followed but the content between the parenthesis was not a link, it would print out the content between the parenthesis. Since this was not a real link, it should have just returned "[]". In order to fix this, we used the "contains()" method to see if there was any empty space between the parethesis, if there was, that meant this was not a link and the loop should break and return nothing. 

***

#### ***Code Change 2:***

*Improper Formating*

![image](https://user-images.githubusercontent.com/100736576/165000879-33a5621e-7d62-4524-a436-bf7d474c1391.png)

[Failure Inducing File](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-file4.md)

***Symptom***
`Exception in thread "main" java.lang.OutOfMemoryError: Java heap space at java.base/java.util.Arrays.copyOfRange(Arrays.java:3822) at java.base/java.lang.StringLatin1.newString(StringLatin1.java:769) at java.base/java.lang.String.substring(String.java:2709) at MarkdownParse.getLinks(MarkdownParse.java:29) at MarkdownParse.main(MarkdownParse.java:40)`
- The issue here was the lack of a set of parenthesis after the brackets. This caused the code to continue running because it was searching for the open parenthesis. In order to fix it, starting from the close bracket, if there was no open parenthesis found, it would break the loop and return nothing.

***

### ***Code Change 3:***
*No closing bracket*

![image](https://user-images.githubusercontent.com/100736576/165003045-e0fead86-6f0b-4682-b2a1-e4f6dcab03e9.png)

[Failure Inducing File](https://github.com/celesteck/markdown-parser/blob/main/test2.md)

***Symptom*** `infinite loop`
![image](https://user-images.githubusercontent.com/100736576/165003144-e3331885-c269-4f90-8e34-45b43657359a.png)
- Here, we can see that the code would not end as it is searching for the close bracket. Since there is no close bracket, in order to fix this, we made an if statement that allowed the code to break the loop if the close bracket was not found. This allowed it to only print out the second link.

