# Lab2-Report
# 1:

- Show a screenshot of the code change diff from Github:
<img width="568" alt="1" src="https://user-images.githubusercontent.com/92092627/151528584-966d790f-eb67-482a-875d-7c18b48e35b1.png">

- Link to the test file for a failure-inducing input that prompted you to make that change: 
(https://github.com/kyy006/markdown-parse/blob/main/test2.md) 

- Show the symptom of that failure-inducing input by showing the output of running the file at the command line for the version where it was failing (this should also be in the commit message history):

  Infinite loop

<img width="696" alt="2" src="https://user-images.githubusercontent.com/92092627/151529758-cb974fcb-0460-4313-8c7b-6d24d237ac65.png">

- Write 2-3 sentences describing the relationship between the bug, the symptom, and the failure-inducing input:

  The symptom is the infinite output. The bug is the loop will keep searching.
  The failure-inducing input is that this test file caused a infinite loop because the code does not know which close parenthesis is last close parenthesis, so the while loop will keep running, so there is infinite loop.

# 2:

- Show a screenshot of the code change diff from Github:

<img width="525" alt="3" src="https://user-images.githubusercontent.com/92092627/151534907-1bcfd059-c27f-44f5-bc54-b50e91e934ba.png">

- Link to the test file for a failure-inducing input that prompted you to make that change: 

https://github.com/kyy006/markdown-parse/blob/main/empty.md

https://github.com/kyy006/markdown-parse/blob/main/MarkdownParseTest.java

- Show the symptom of that failure-inducing input by showing the output of running the file at the command line for the version where it was failing (this should also be in the commit message history):

The junit test failed.

<img width="730" alt="4" src="https://user-images.githubusercontent.com/92092627/151532353-3533c813-9d5d-42ff-8705-f77381deaa42.png">

- Write 2-3 sentences describing the relationship between the bug, the symptom, and the failure-inducing input:

  The symptom is junit test failed. The bug is wrong code in the try catch test method. 
  The failure-inducing input: we need to figure out how to use try catch and know how the test method can catch exception first, so we changed the file to empty file and search empty string.
