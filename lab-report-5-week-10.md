My markdown-parse repository: [link](https://github.com/kyy006/markdown-parse)

<img width="694" alt="mycode" src="https://user-images.githubusercontent.com/92092627/157802593-a64b77d2-c7d6-4856-a6c4-dc8d12478013.png">

run this command for both file:
`bash script.sh > results.txt`

<img width="681" alt="runtestresult" src="https://user-images.githubusercontent.com/92092627/157802839-649f1a40-fa1f-46bd-8ece-3ebe1d9fe3d6.png">


How you found the tests with different results (Did you use diff on the results of running a bash for loop? Did you search through manually? Did you use some other programmatic idea?):

I used the `diff mymarkdown1/results.txt markdown-parse/results.txt` to find the different results, `mymarkdown1` is my implementation, `markdown-parse` is the implementation provided for lab 9.

<img width="515" alt="runtestresult" src="https://user-images.githubusercontent.com/92092627/157803784-6fc587c0-9db7-49fb-a39a-5534372f13e8.png">
