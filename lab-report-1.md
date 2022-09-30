# Lab Report 1

Today we will learn how to connect a device to a remote server and upload files to run on it. These simple steps below will help guide you through the process.

## Step 1: Download VSCode
* VSCode is the text editor we will be using to write a java program that will upload to our remote server. 
* To download VSCode, go to the VSCode page on your preferred browser and download the file corresponding to your device's operating system. 

## Step 2: Remote Connecting
* Open up terminal on your computer 
* Run the ssh command using your unique username to connect to establish remote connection
*       <ssh [username]@ieng6.ucsd.edu>
* You will be prompted to enter your password to log into the remote connection

## Step 3: Try Some Commands
* Practice running some commands such as ls or cd, both are useful when it comes to managing your directory 
* *  < ls > opens up a list of directories under the current directory 
* * < cd > changes the directory you are in

## Step 4: Moving Files with scp
* To move a file over ssh with scp start on your computer and open terminal in the directory where the file is located 
* Next enter the scp command to upload the file to the remote location
*       < scp [file name][username]@ieng6.ucsd.edu:~/>
* * Note: this command puts the file into the home directory, to add to a specific location add the directory following the last forward slash (/)
* You will then prompted to enter your password to complete the upload

## Step 5: Creating SSH Key
* First on your computer terminal enter the following command 
*       < ssh-keys >
* You will then be prompted to enter a file to save the key, simply hit enter again to set it to the default path
Next, when it says enter passphrase, hit enter to leave it blank. 
* Hit enter again for confirmation of the empty passphrase
* Then, log onto the remote location using ssh and create a new directory called .ssh to store the key 
*       < mk dir .ssh>
* Next, copy the public key to the remote location using scp
*       < scp [location of key] [username]@ieng6.ucsd.edu:~/.ssh/authorized_keys 
* You should now be able to log into the remote location using ssh without having to enter a password
## Step 6: Optimization
* To run commands faster in terminal you can use a semicolon (;) to separate lines of code 
* You can also use the up arrow key to rerun some previous commands, this will make it easier to scp files or use ssh to login without having to type the same thing over and over again

