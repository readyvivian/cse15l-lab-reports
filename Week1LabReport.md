# Week 1 Lab Report
Vivian Wang | A17457779 | v8wang@ucsd.edu
## Step 1: Installing VScode
1. Visit: [Visual Studio Code website](https://code.visualstudio.com/).
2. Download and install Visual Studio Code.
3. Open a window:
    
    <img width="759" alt="image" src="https://user-images.githubusercontent.com/122570273/212195532-9f4470a7-f781-4f4e-9174-e888fca28fa2.png">
## Step 2: Remotely Connecting
1. Open a terminal in VScode.
2. Type the command and replace `cs15lwi23zz` with the course-specific account:
    
    ```
    $ ssh cs15lwi23zz@ieng6.ucsd.edu
    ```
3. If you get the message:
    
    ```
    The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established.
    RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.
    Are you sure you want to continue connecting (yes/no/[fingerprint])?
    ```
    Type `yes`.
4. Type your password after `Password: ` and press enter: (You won't see anything while typing)
5. You will see:
    
    <img width="484" alt="image" src="https://user-images.githubusercontent.com/122570273/212195449-ecfabbc8-7cb8-41cb-ba3c-39c61276f537.png">
    
    Now your terminal is remotely connected to a computer in the CSE basement.
## Step 3: Trying Some Commands
Try to run some command, e.g.:
* `cd` Change working directory.
* `ls` List the files and folders in the current working directory.
* `cat /home/linux/ieng6/cs15lwi23/public/hello.txt` Print the contents of the file.
<img width="560" alt="image" src="https://user-images.githubusercontent.com/122570273/212197520-c821936b-3b5e-4e37-965c-53e05fc53fc8.png">
