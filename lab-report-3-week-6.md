# **Lab Report 3**

## Streamlining `ssh` Configuration   
- We start by navigating to the ssh directory `cd ~/.ssh` where we create a config file to be used
*(because my laptop is operating via Windows I used git bash to do this)*
#### `.ssh/config` file
- ![image](https://user-images.githubusercontent.com/100736576/167277434-11a1cd33-fadd-4dd9-8c16-facf49fd06c4.png)

- I made the file inside git bash where I allowed ieng6 to be my alias 
#### logging in with an alias *ieng6*
-  ![image](https://user-images.githubusercontent.com/100736576/167277551-a966e257-7917-4fd7-9026-d182d0f51d41.png)

- Then I create a newfile called `newfile` on my local computer and then usec `scp` to copy it over to the remote server!
#### `scp` command copying a file 
- ![image](https://user-images.githubusercontent.com/100736576/167278602-75531f4d-e7a5-479b-bde0-a663cd187e85.png)

***
## Github access from `ieng6`

- The public key you made will be found in the `SSH and GPG keys` tab under **Access**
- ![image](https://user-images.githubusercontent.com/100736576/167279559-be68c1a5-80f4-4eea-b52a-a9a915e6f85e.png)

- This is what it looks like on my user account:
- ![image](https://user-images.githubusercontent.com/100736576/168512660-ca1f3bc1-dcf2-4b4b-ae4a-04ab2a2c19e4.png)

-In order to find the private key, you can change your directory to `ssh`, then you can `ls` and you can see it in your current directory
![image](https://user-images.githubusercontent.com/100736576/168501168-29e5c292-f6db-4cad-915c-cdc2ed47110e.png)


- Now if we log into our `ieng6` account we can use git commands to commit and push changes
- ![image](https://user-images.githubusercontent.com/100736576/168508447-9e0c52b2-807e-4bdf-8da2-9530f675942e.png)



[here is the resulting commit](https://github.com/celesteck/cse15l-lab-reports/commit/6ec3b257a20aa2e110317f707f897f6cd6124ad2)

***
## Copy whole directories with `scp -r`

- By inputting `scp -r . cs15lsp22agl@ieng6.ucsd.edu:~/markdown-parse` into the terminal, this is is how I can copy the entire directory into my `ieng` account as shown here
 ![image](https://user-images.githubusercontent.com/100736576/167313026-26387b62-2874-4526-b557-2ba549ded236.png)
- Now I can log into my `ieng6` account using `ssh` and see all of these files in my directory also called **markdown-parse**
![image](https://user-images.githubusercontent.com/100736576/167313625-4c937f5d-85a9-479a-a1f0-03e973bb1f09.png)

- To simplify this process we can use the `ssh` command and the `scp` commands in one line using a **;**
- The command looks like this : `scp -r *.java *.md lib/ ieng6:markdown-parse ssh cs15lsp22aay@ieng6.ucsd.edu; javac -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar MarkdownParseTest.java; java -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar org.junit.runner.JUnitCore MarkdownParseTest`
- ![image](https://user-images.githubusercontent.com/100736576/168512264-81a3d0b1-0b5e-4dd4-8d20-97a19b7d9ed5.png)
- Because I streamlined the ssh configuration as seen earlier, I am able to just use ieng6, my *alias*.





