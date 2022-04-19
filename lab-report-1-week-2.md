# How To Log Into a Course-Specific Account On `ieng6`


### Step One:
*Installing VSCode*

- Download VSCode [here:](https://code.visualstudio.com/download)

- Once you open it, it should look like this:
-![image](https://user-images.githubusercontent.com/100736576/162540822-57c32eb7-c96e-4605-ac65-d279474423d8.png)

 
- Here you can open a new file in the top left corner and name it
      *if you are using java use:* ` .java`
      
***

**Step Two:**
### Remotely Connecting

- Install a program called OpenSSH [here](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse)

- Once installed and you have found your course-specific account, open a terminal in VSCode
  and input this command `ssh cs15lsp22agl@ieng6.ucsd.edu`
  
  It will prompt you to answer a y/n question, say yes and type in your password!
  You are now connected :D
  ![image](https://user-images.githubusercontent.com/100736576/162541027-d3e755ec-e9f3-4aa7-8c21-9bf325a671f1.png)

***  
  
  
**Step Three:**
Trying Some *Commands*

- Here are some commands we ran:
  - `cd`
  - `cd ~`
  - `ls`
  - `ls -lat`
 ***
 - Here is how some of these commands work:
    - cd means change directory
    - ls shows us a list of everything in the directory
    - cat prints out the output of the file
 
 After running these commands, your terminal might look like this:
 ![image](https://user-images.githubusercontent.com/100736576/162541845-e4203bc9-06f8-4ad3-b3af-bd5ed0b58ab9.png)

***

Step **Four:**
*Moving files with* `scp`
***
- In this step we are going to see how we can move files over from our own personal computer to the remote- computer:
                                                                                                                     
- Lets make a file to try with called **WhereAmI.java**
- ![image](https://user-images.githubusercontent.com/100736576/162542185-850d2e29-0840-4c4b-b268-f1ec948b8201.png)

- In the terminal put:  `scp WhereAmI.java cs15lsp22agl@ieng6.ucsd.edu:~/` and input your password
- You can now log into the ieng6 and see the file there when you use the `ls` command
- This means you can now run the file on the remote computer and your own computer using `.javac` and `.java`

Here it is on a split terminal:
![image](https://user-images.githubusercontent.com/100736576/162542806-8f5caeaf-b96b-494b-b7cb-133332d81484.png)

***
## **Step Five:**
### *Setting an SSH key*
***
- In this step we will see how to use a key rather than our password to log in and run `scp`

1. Begin on your computer and run `sshk-keygen`. Do not set a passphrase and press enter
2. Then run `ssh cs15lsp22agl@ieng6.ucsd.edu` and enter your password
3. Run `mkdir .ssh` 
4. Run `scp /Users/<celes>/.ssh/id_rsa.pub cs15lsp22agl@ieng6.ucsd.edu:~/.ssh/authorized_keys` 
5. Now you can `ssh` or `scp` with no password

When you log in, it will look like this;
![image](https://user-images.githubusercontent.com/100736576/162543561-f2458ee6-130a-45a0-8bcc-ba2fb3a741a6.png)

***

## **Step Six:**
### *Optimizing Remote Running*
***
- In this step we will make this process even quicker. This is especially helpful when making edits locally on your file.
- We can learn that special syntax that will make running code faster
   1. put the command in "quotes" at the end of an ssh command to run it on the remote server
   2. use semi-colons to run multiple commands on the same line
      ![image](https://user-images.githubusercontent.com/100736576/162549238-39a6a750-4a4e-46b7-ae90-5791ae90cba9.png)

      
