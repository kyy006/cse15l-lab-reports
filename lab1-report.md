# Lab1-Report
# 1.Setting up VScode:

<img width="1920" alt="3" src="https://user-images.githubusercontent.com/92092627/149395772-85110b67-1372-4489-ae4b-7ebb4317c155.png">

I have installed the VScode in my previous class, so I dont have to install that again, but we can go to the website [https://code.visualstudio.com/](https://code.visualstudio.com/)

# 2.Remotely Connecting:

<img width="496" alt="4" src="https://user-images.githubusercontent.com/92092627/149397446-4ead17ca-0a8e-4c7d-9831-82e21e73df93.png">

I have to look up my account and reset my password on the website [https://sdacs.ucsd.edu/~icc/index.php](https://sdacs.ucsd.edu/~icc/index.php), then I can log in to the server by using (`ssh cs15lwi22aed@ieng6.ucsd.edu`)After I logged in , it showed I logged into ieng6-203.ucsd.edu, I believe it is a server. And it also told me how many percent of the CPU I am using. It also showed the “Cluster Status”, I believe these are different servers of the connection, and it also showed the Users,Load,Averages, which means the load of CPU usage.

# 3.Trying Some Commands:

<img width="497" alt="2" src="https://user-images.githubusercontent.com/92092627/149397180-1123efab-6652-4a87-8cf7-ae939a0bce23.png">

Then I type `cd ..`, it showed me `cs15lwi22:2$`, I think it is part of our username.
<img width="708" alt="9" src="https://user-images.githubusercontent.com/92092627/151502274-eb2b5304-3291-4ea5-b3ff-79ce07a3a491.png">

I also tried some other commands
(`cp WhereAmI.java OtherMain.java`)
(`javac OtherMain.java`)
(`java WhereAmI`)
<img width="724" alt="10" src="https://user-images.githubusercontent.com/92092627/151507413-3e9b06d5-fc88-4c0b-a80d-85e6d039b6d4.png">

I also tried these commands:
`cd ~`
`cd`
`ls -lat`
`ls -a`

<img width="713" alt="11" src="https://user-images.githubusercontent.com/92092627/151507773-fa881519-4856-4ba8-8aa7-4a4d6f5ce4e3.png">


I also tried these commands:

`ls <directory>` where <directory> is /home/linux/ieng6/cs15lwi22/cs15lwi22abc, where the abc is one of the other group members’ username
  
`cp /home/linux/ieng6/cs15lwi22/public/hello.txt ~/`
`cat /home/linux/ieng6/cs15lwi22/public/hello.txt`
# 4.Moving Files with scp:

<img width="497" alt="5" src="https://user-images.githubusercontent.com/92092627/149397976-c49bc107-ab50-4bc8-85eb-fce40117009c.png">

I created a java file on my own computer called "whereAmI.java", then I use `scp WhereAmI.java cs15lwi22aed@ieng.ucsd.edu` to copy the file to the server. Then I log in to my account to check if the file exists. I saw the file existing on the server.

# 5.Setting an SSH key:

<img width="602" alt="6" src="https://user-images.githubusercontent.com/92092627/149402903-83d32368-2221-4e8f-a468-78c037fb0e26.png">

I followed the instructions for window in powershell.
For Windows, follow the extra ssh-add steps here: [link](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_keymanagement#user-key-generation)

<img width="898" alt="7" src="https://user-images.githubusercontent.com/92092627/149403706-4d3be889-758e-4857-8c55-3a287aa3a743.png">

Then I followed the instructions and type the command in VScode, Then I can do ssh and scp without entering my passport.
`ssh cs15lwi22aed@ieng6.ucsd.edu`-->Enter Password-->`mkdir .ssh`-->`logout`-->`scp /C:\Users\User/.ssh/id_rsa.pub cs15lwi22aed@ieng6.ucsd.edu:~/.ssh/authorized_keys`
After these code, I can login to my account without password.

# 6.Optimizing Remote Running:

<img width="638" alt="8" src="https://user-images.githubusercontent.com/92092627/149407297-335352a2-88f0-42d4-9636-1773deeb701d.png">

I tried few command to make remote running, and I also use semicolons to run multiple commands on the same line. I tried 10 commands including all typing, the total time will be 3mins.
(`ssh cs15lwi22aed@ieng6.ucsd.edu "ls"`)
(`ssh cs15lwi22aed@ieng6.ucsd.edu "cd"`)
(`ssh cs15lwi22aed@ieng6.ucsd.edu "ls -a"`)
(`ssh cs15lwi22aed@ieng6.ucsd.edu "ls -lat"`)
(`ssh cs15lwi22aed@ieng6.ucsd.edu "cd .."`)
(`cp WhereAmI.java OtherMain.java; javac OtherMain.java; java WhereAmI`)
(`cp WhereAmI.java OtherMain123.java; javac OtherMain.java; java WhereAmI`)
(`cp WhereAmI.java Other123Main.java; javac OtherMain.java; java WhereAmI`)
