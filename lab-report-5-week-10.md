My markdown-parse repository: [link](https://github.com/kyy006/markdown-parse)

<img width="694" alt="mycode" src="https://user-images.githubusercontent.com/92092627/157802593-a64b77d2-c7d6-4856-a6c4-dc8d12478013.png">

run this command for both file:
`bash script.sh > results.txt`

<img width="681" alt="runtestresult" src="https://user-images.githubusercontent.com/92092627/157802839-649f1a40-fa1f-46bd-8ece-3ebe1d9fe3d6.png">


How you found the tests with different results (Did you use diff on the results of running a bash for loop? Did you search through manually? Did you use some other programmatic idea?):

I used the `diff mymarkdown1/results.txt markdown-parse/results.txt` to find the different results, `mymarkdown1` is my implementation, `markdown-parse` is the implementation provided for lab 9.

<img width="515" alt="runtestresult" src="https://user-images.githubusercontent.com/92092627/157803784-6fc587c0-9db7-49fb-a39a-5534372f13e8.png">


two tests are different:

<img width="219" alt="pick2" src="https://user-images.githubusercontent.com/92092627/157804163-1428c11d-6b50-42e3-af21-a74891353550.png">


first one:

The first different happened on line 270. So we want to open the results.txt to see which file belongs to.

`cd mymarkdown1` > `vim results.txt` > `:set number`

Then we can see the results.txt with line number, and that’s the test output for the file `22.md`

In my implementation:

<img width="466" alt="findmd" src="https://user-images.githubusercontent.com/92092627/157805250-5a53acc1-f5f2-4aaf-8725-3fc4b37a3e41.png">

` 269 test-files/22.md`
`270 [/bar\* "ti\*tle"`

Provided implementation:

![image](https://user-images.githubusercontent.com/92092627/157805598-7edd9194-fc05-48e4-9f6c-fd2d965fe9ea.png)




second one:
The first different happened on line 492. And we do the same thing to check which file belongs to.

`cd mymarkdown1` > `vim results.txt` > `:set number`

Then we can see the results.txt with line number, and that’s the test output for the file `32.md`

In my implementation:

![image](https://user-images.githubusercontent.com/92092627/157806025-cea7476e-e16b-4d18-8f50-6131f149948e.png)


Provided implementation:

![image](https://user-images.githubusercontent.com/92092627/157805841-138f0886-370a-438a-9cca-0320e96aa77b.png)


Looked at the input file to use our judgment to tell what the expected output should be:

![image](https://user-images.githubusercontent.com/92092627/157806488-7d6e19bf-1344-4536-9860-1ee8ddc31b6b.png)


For test1 comparsion(22.md):
Describe which implementation is correct, or if you think neither is correct, by showing both actual outputs and indicating what the expected output is.

Joe's implementation is correct, because this should not be a link. Jose has the expected output.

For the implementation that’s not correct (or choose one if both are incorrect), describe the _bug (the problem in the code). You don’t have to provide a fix, but you should be specific about what is wrong with the program, and show the code that should be fixed.

I think there is a slash after the open Bracket, and also there are some other sign or marks inside the Bracket, so what we need to fix is, for example If we see a `*` inside the Bracket, then we should not print anything, because a link should not have some kind of sign or mark.
![image](https://user-images.githubusercontent.com/92092627/157807325-c05790ff-1102-41a1-9e8d-3645c3c6a16f.png)
I think we should set some more condition in to the if statement(yellow circle), and we should also set up another if statement to check any sign/mark that not expected inside the Bracket, then the current index should jump to another open Bracket or end the method. Also we should check if there is a slash after the open Bracket, if so , then dont print this bracket.


For test2 comparsion(32.md):
Describe which implementation is correct, or if you think neither is correct, by showing both actual outputs and indicating what the expected output is.

Joe's implementation is correct, because this should not be a link. Jose has the expected output.

For the implementation that’s not correct (or choose one if both are incorrect), describe the _bug (the problem in the code). You don’t have to provide a fix, but you should be specific about what is wrong with the program, and show the code that should be fixed.

I think I have same problems with this test case, there are a lot of sign/mark we dont expect show up inside the bracket,such as double Question Mark.
I think there is a slash after the open Bracket, so what we need to fix is, for example If we see double Question Mark inside the Bracket, then we should not print anything, because a link should not have double Question Mark.
![image](https://user-images.githubusercontent.com/92092627/157807325-c05790ff-1102-41a1-9e8d-3645c3c6a16f.png)
I think we should set some more condition in to the if statement(yellow circle), and we should also set up another if statement to check any sign/mark that not expected inside the Bracket, then the current index should jump to another open Bracket or end the method. Also we should check if there is a slash after the open Bracket, if so , then dont print this bracket.
