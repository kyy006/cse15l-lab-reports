# Lab6-Report

Option1 :Streamlining ssh Configuration
Since I am using Window, there are few more steps that I need to do to set up ssh Configuration.

# First
In the left side, find the Extension button, and press it. Then search "Remote-SSH", and install it.

<img width="958" alt="1" src="https://user-images.githubusercontent.com/92092627/153644201-722e7351-dcbb-4f35-958c-ad6d273145ee.png">

Press `Ctrl+p` on your keyboard, the search box will come out and search `>ssh`, press the "Remote-SSH: connect to the host"
<img width="912" alt="2" src="https://user-images.githubusercontent.com/92092627/153644571-a009a2e9-b221-413b-9bcd-5a4fc9f031a0.png">


Then press "Add New SSH Host", then the box ask you to type your SSH
<img width="956" alt="3" src="https://user-images.githubusercontent.com/92092627/153644829-3edb2b64-09d4-422d-921b-95d7f6cdf501.png">


type `ssh cs15lwi22aed@ieng6.ucsd.edu`
<img width="944" alt="4" src="https://user-images.githubusercontent.com/92092627/153644952-0275e87c-6160-4286-8290-56c162529e82.png">

choose and press the first option, which is the location of my ssh file
<img width="953" alt="5" src="https://user-images.githubusercontent.com/92092627/153645163-7df8c91f-e467-4f77-9748-55e9fe954249.png">


On the lower right buttom, press "the Open Config"
<img width="956" alt="6" src="https://user-images.githubusercontent.com/92092627/153645306-93f0cba9-819b-498d-b3d3-37db8b7092c7.png">

Then this file will come out, then Type `IdentityFile C:\Users\User\.ssh\id_rsa` on the line 4.
<img width="952" alt="7" src="https://user-images.githubusercontent.com/92092627/153645679-334c8ff7-c6e1-4c09-8aea-a4df7185ef69.png">
<img width="689" alt="8" src="https://user-images.githubusercontent.com/92092627/153645687-8ef25de9-476b-4b39-8299-159205af0624.png">

Then we can type the `ssh ieng6` in the terminal, log in to the server.
<img width="526" alt="9" src="https://user-images.githubusercontent.com/92092627/153645841-b1832ba6-c8c2-4fdc-a05e-1956ad142b14.png">



