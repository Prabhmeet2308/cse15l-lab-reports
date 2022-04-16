**LAB Report 1**

To start with the cse lab before the 1st lab change your password by following the guide provided by the professor

During the first lab the first step would be to

**Install VSCode.**

For that go to [VSC Download Link](https://code.visualstudio.com/) .Install the version for your operating system for me it was OSX(for mac). After downloading install the file in your application folder(for mac).
This is what the VSC looks like

 ![LAB1-1](https://user-images.githubusercontent.com/103228599/162647026-6ae9bd7f-13ff-457b-8379-c4052504947e.png)
 
 **Remotely Connect**
 
To remotely connect you would need the course specific account for CSE 15L class 
Then open the terminal and type the following command ``` ssh cs15lsp22zz@ieng6.ucsd.edu ``` and replace zz with your course specific account
After this if it is your first time connecting to a server you will get a message about authenticity reply yes to that message.

![LAB1-2](https://user-images.githubusercontent.com/103228599/162647047-1d002966-fdd1-402b-8969-7c028a356429.png)


**Trying Some Commands**

After successfully logging in try some commands on both your computer and the remote computer. Some of these commands include ```cd``` , ```ls``` and their variations like ```ls -a``` , ```ls -l``` , ```ls -t``` also command exit when logged in remote computer. You can have multiple terminals on VSCode which can be very helpful.

![LAB1-3](https://user-images.githubusercontent.com/103228599/162647070-dce7f24f-94a9-4b03-b89a-3047e76f3cc8.png)

![LAB1-4](https://user-images.githubusercontent.com/103228599/162647071-130d363b-7ec6-4397-a788-205144942ef9.png)



**Moving files with scp**

We’ll now see another way to copy a file (or many files!) from your computer to a remotecomputer. The command is called scp. We run it from client that is your computer. Take a file say WhereAmI.java for example the command would be 
```scp WhereAmI.java cs15lsp22zz@ieng6.ucsd.edu:~/``` (replace zz with account name)
It will prompt you for ieng6 password and use ls to check if the file was transferred

 ![LAB1-5](https://user-images.githubusercontent.com/103228599/162647137-8034f546-d104-450d-9a6d-d7858bf40969.png)

**Setup SSH Keys**

To avoid entering password every time you login or run scp command  we set ssh keys.
On your client enter ssh-keygen command then enter the file to save the key. Then it will prompt for enter passphrase which should be left empty. After that follow the following commands
```
“ssh cs15lsp22zz@ieng6.ucsd.edu
Enter Password
# now on server
$ mkdir .ssh
$ logout
# back on client
$ scp /Users/user-name/.ssh/id_rsa.pub
cs15lsp22zz@ieng6.ucsd.edu:~/.ssh/authorized_keys”
```
![LAB1-6](https://user-images.githubusercontent.com/103228599/162647147-bc544f73-3415-4040-b2f0-08d4d0f648af.png)
![LAB1-7](https://user-images.githubusercontent.com/103228599/162647153-04dad844-175d-446b-ab6d-91c460565a3d.png)


**To optimize remote running**

To optimize you can write a command at the end of the ssh command to directly run it on the remote server. You can use semicolons to run multiple commands together. You can also use the up arrow key on your keyboard to recall previous command to save time.
 ![LAB1-8](https://user-images.githubusercontent.com/103228599/162647154-06ed2ef0-5573-4a01-84f8-fe0c895aaf51.png)
 
