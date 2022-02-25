My markdown-parse repository: [link](https://github.com/kyy006/markdown-parse)

<img width="698" alt="mymark" src="https://user-images.githubusercontent.com/92092627/155770147-14680967-1815-47cb-b38a-80d3deac372f.png">


The one I reviewed:[link](https://github.com/jdweak/markdown-parse/blob/main/MarkdownParse.java)

<img width="688" alt="reviewmark" src="https://user-images.githubusercontent.com/92092627/155770152-ddef87ba-6ede-4a3a-ad2e-8447c709e985.png">

Decide on what it should produce by using either VScode preview:

<img width="699" alt="expectString" src="https://user-images.githubusercontent.com/92092627/155786005-aab33712-8aa2-4db5-9bba-9a9a2cc78ff3.png">

There will be 3 expected link of string on each snippet

My `MarkdownParseTest.java` file:

<img width="699" alt="testfile" src="https://user-images.githubusercontent.com/92092627/155788739-6bde5f99-e481-42a8-b720-655f7dbdafee.png">

Then type these 2 command to test our code:

`javac -cp ".;lib\junit-4.13.2.jar;lib\hamcrest-core-1.3.jar" MarkdownParseTest.java`

`java -cp ".;lib/junit-4.13.2.jar;lib/hamcrest-core-1.3.jar" org.junit.runner.JUnitCore MarkdownParseTest`


shows the test failure:

<img width="687" alt="runtest" src="https://user-images.githubusercontent.com/92092627/155788821-81d3f389-90a1-4076-beea-ae1cb380d495.png">


`testFile1`,`testFile3`,`testFile5`  corresponding to my MardownParse.java

`testFile2`,`testFile4`,`testFile6`  corresponding to the one I reviewed

So, for my implementation and the implementation that I reviewed failed to pass all tests.

Answer the following questions with 2-3 sentences each:
1.Do you think there is a small (<10 lines) code change that will make your program work for snippet 1 and all related cases that use inline code with backticks? If yes, describe the code change. If not, describe why it would be a more involved change.

Yes, I think there are two backticks to make the text inside that to be code text and different front of text, we should check this condition to avoid that. If there is code text, then we should not treat this as a link. but my code treat this as a link.



2.Do you think there is a small (<10 lines) code change that will make your program work for snippet 2 and all related cases that nest parentheses, brackets, and escaped brackets? If yes, describe the code change. If not, describe why it would be a more involved change.

yes,my code seems like only can return one string, from the failed test, `java.lang.AssertionError: expected:<[a.com]> but was:<[a.com, a.com(()), example.com]>`, I have the first element of the expected string , but there are other two missing, I should change my code to invole the others.



3.Do you think there is a small (<10 lines) code change that will make your program work for snippet 3 and all related cases that have newlines in brackets and parentheses? If yes, describe the code change. If not, describe why it would be a more involved change.

yes,my code seems like only can return one string, from the failed test, `java.lang.AssertionError: expected:<[https://www.twitter.com]> but was:<[https://www.twitter.com, https://ucsd-cse15l-w22.github.io/, https://cse.ucsd.edu/]>`, I have the first element of the expected string , but there are other two missing, I should change my code to invole the others.

