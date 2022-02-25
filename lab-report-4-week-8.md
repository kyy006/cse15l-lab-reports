My markdown-parse repository: [link](https://github.com/kyy006/markdown-parse)

<img width="698" alt="mymark" src="https://user-images.githubusercontent.com/92092627/155770147-14680967-1815-47cb-b38a-80d3deac372f.png">


The one I reviewed:[link](https://github.com/jdweak/markdown-parse/blob/main/MarkdownParse.java)

<img width="688" alt="reviewmark" src="https://user-images.githubusercontent.com/92092627/155770152-ddef87ba-6ede-4a3a-ad2e-8447c709e985.png">

Decide on what it should produce by using either VScode preview:

<img width="699" alt="expectString" src="https://user-images.githubusercontent.com/92092627/155786005-aab33712-8aa2-4db5-9bba-9a9a2cc78ff3.png">

There will be 3 expected link of string on each snippet

My `MarkdownParseTest.java` file:

<img width="704" alt="testfile" src="https://user-images.githubusercontent.com/92092627/155785670-cf8d6bd6-6253-4276-a467-8c8cf87fac63.png">


Then type these 2 command to test our code:

`javac -cp ".;lib\junit-4.13.2.jar;lib\hamcrest-core-1.3.jar" MarkdownParseTest.java`

`java -cp ".;lib/junit-4.13.2.jar;lib/hamcrest-core-1.3.jar" org.junit.runner.JUnitCore MarkdownParseTest`


shows the test failure:

<img width="693" alt="runtest" src="https://user-images.githubusercontent.com/92092627/155785689-bf1f00ff-6720-4dd5-b6a3-5f3c029d87a5.png">


`testFile1`,`testFile3`,`testFile5`  corresponding to my MardownParse.java

`testFile2`,`testFile4`,`testFile6`  corresponding to the one I reviewed

So, for my implementation and the implementation that I reviewed failed to pass all tests.

Answer the following questions with 2-3 sentences each:
Do you think there is a small (<10 lines) code change that will make your program work for snippet 1 and all related cases that use inline code with backticks? If yes, describe the code change. If not, describe why it would be a more involved change.

Yes, I think there are two ` to make the text inside that to be code text and different front of text, we should check this condition to avoid that. If there is code text, then we should not treat this as a link. but my code treat this as a link.
Also, my code seems like only can return one string


Do you think there is a small (<10 lines) code change that will make your program work for snippet 2 and all related cases that nest parentheses, brackets, and escaped brackets? If yes, describe the code change. If not, describe why it would be a more involved change.
Do you think there is a small (<10 lines) code change that will make your program work for snippet 3 and all related cases that have newlines in brackets and parentheses? If yes, describe the code change. If not, describe why it would be a more involved change.
