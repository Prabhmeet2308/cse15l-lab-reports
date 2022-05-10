# Lab Report 3


## Streamlining ssh Configuration
We first opened our terminal where we typed ```cd .ssh``` to go into our ```.ssh```  files. We then used the ```vim```command to make a new file called ```"config"``` where we typed in our ssh username and host. We saved and exited the new file by pressing esc key then inputting ```":wq!"```. At that point, all we needed to do was type in ```"ssh ieng6"``` into the command line, and it automatically connects us to the other server.
### Config File
![WhatsApp Image 2022-05-07 at 5 51 39 PM](https://user-images.githubusercontent.com/103228599/167344014-9bdc21ab-33f3-4620-bd03-60cef00b5fa3.jpeg)


### ssh Login
![WhatsApp Image 2022-05-07 at 5 49 43 PM](https://user-images.githubusercontent.com/103228599/167344135-040dd25b-4749-43dd-9ebb-af8a3d22f190.jpeg)

### scp Command with Login
![WhatsApp Image 2022-05-07 at 5 47 35 PM](https://user-images.githubusercontent.com/103228599/167344173-6d29465f-a912-4947-bffc-7d7069eab170.jpeg)




## Setup Github Access from ieng6

### Public Key on Github
First we needed to get our ssh public key. So in order to do that you first need to go to your terminal, type in ```cd .ssh``` and then ```ls.``` If any of the files named: ```id_rsa.pub, id_ecdsa.pub, id_ed25519.pub``` are there; then just type ```pbcopy<~/.ssh/(filename)``` to copy it. Mine was ```pbcopy<~/.ssh/id_rsa.pub```. Note that the ones with ```.pub``` are the public SSH keys.
Then go to Github page from there go to settings-> SSH and GPG keys-->click on the green "New SSH key" button. It will then ask you for the title(which can be anything), and the actual key itself, that is what you just copied.

![WhatsApp Image 2022-05-07 at 5 54 14 PM](https://user-images.githubusercontent.com/103228599/167344322-d81e68ec-0e3b-42d7-9593-f175c38f4399.jpeg)


### Private Key on Sever
![WhatsApp Image 2022-05-07 at 5 53 51 PM](https://user-images.githubusercontent.com/103228599/167344395-6b484249-072e-46d6-88da-0a9d5857552a.jpeg)


### Running git Commmands
<img width="916" alt="Screenshot 2022-05-08 at 10 16 14 PM" src="https://user-images.githubusercontent.com/103228599/167345015-09ce77e7-b459-4a27-a8f0-b800c4252642.png">

### [link to the resulting commit](https://github.com/Prabhmeet2308/markdown-parser/commit/f2a1149135dfd6f1e15432b339b2c6f725177e63)


## Copy whole directories with scp -r
We can use scp to copy a directory(represented by .) to the remote server. We also have to give a name of the directory we want it to copy into on the remote server:
```"$ scp -r . cs15lsp22@ieng6.ucsd.edu:~/markdown-parse"```
The ```"-r"``` option tells ```"scp"``` to work recursively. The ```"."``` is the source, and is the current directory. The ```"~/markdown-parse"``` tells scp to create the markdown-parse directory on the remote server (if it doesn’t exist), and then copy the contents of this directory recursively there.
If we do this, then we can log into the server with ```"ssh"``` and see all of our files there in a
directory called markdown-parse:
### Copying markdown-parse
<img width="1151" alt="Screenshot 2022-05-08 at 11 24 57 PM" src="https://user-images.githubusercontent.com/103228599/167352148-89919f62-5afa-4c5f-8738-5d8e3ced53c9.png">
<img width="1134" alt="Screenshot 2022-05-08 at 11 25 36 PM" src="https://user-images.githubusercontent.com/103228599/167352211-45411b80-991c-4a99-b3d3-2f2139448d38.png">


### Running tests
<img width="1348" alt="Screenshot 2022-05-08 at 10 56 19 PM" src="https://user-images.githubusercontent.com/103228599/167348896-62c5e97a-a753-4894-98a7-4b73927cc480.png">


### Combining scp
<img width="1146" alt="Screenshot 2022-05-08 at 11 29 27 PM" src="https://user-images.githubusercontent.com/103228599/167352681-c85bf597-e727-428f-84c5-3b29b0a5863a.png">
<img width="1136" alt="Screenshot 2022-05-08 at 11 29 42 PM" src="https://user-images.githubusercontent.com/103228599/167352710-86d131be-89dd-40a2-8725-8b6429869cac.png">


