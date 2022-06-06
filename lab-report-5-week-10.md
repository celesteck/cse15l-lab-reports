# Lab Report 5

***
### **Finding Tests With Different Results**
- To find the descrepancies betweeen the tests, I first made a copy of the test file directory in my markdown parser
- I then ran `bash script.sh > results.txt`. This allows me to run the files with the script, then print the results and save it to a file
- I did this in the other repository and then used `vim diff` to open both files in order to compare them.

### TEST 1
- [Link to test170](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/170.md)
***

![image](https://user-images.githubusercontent.com/100736576/172103066-04fe8b38-6528-4e00-a2e0-6108bbefa28b.png)

This is what is supposed to be printed out:
- ![image](https://user-images.githubusercontent.com/100736576/172107298-46e39eeb-4e61-4e77-ad92-4885f8e142e6.png)

- But as we can see this is not what is returned.  It's not the correct output that I wanted, but something is still printed out. This means that the code functional, but it printed the wrong thing. Since there are open and closed parenthesis around demo, it is likely that is the reason why my code had printed it out. 
***

### TEST 2
- [Link to test376](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/376.md)

- ![image](https://user-images.githubusercontent.com/100736576/172113785-5186c613-7160-4b72-b2ae-5856a8967caa.png)

This is what is supposed to be printed out:
- ![image](https://user-images.githubusercontent.com/100736576/172114347-5c43994b-5e59-4903-a22d-3cd442ec8142.png)

- But as we can see, this is not what is returned here either. Analogous to the other test, it is likely because bar is within the parenthesis and for this reason my code has printed it out. My code does not have an extreme error. 
