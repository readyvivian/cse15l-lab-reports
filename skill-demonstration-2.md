Log into ieng6 with the provided account. Your proctor will provide instructions on logging in; you will not use your own course-specific account, but rather one that we provide. All of the remaining steps involving running commands should be completed from ieng6.
ssh


Clone this autograder repository on ieng6: https://github.com/ucsd-cse15l-w23/grader-skill-demo2
git clone

Compile and start the server on ieng6.
cd g[tab]
javac *Server.java
java GradeServer 1234

Here is a sample student repository with a bug: https://github.com/ucsd-cse15l-w23/list-examples-duplicates. Show the result of grading this with the autograder in a browser or using curl from another terminal logged into ieng6. You must use the http://ieng6-20... URL to load it. It should show all tests passing. (When we say “show the result of running...” below, we always mean in a browser or with curl).
http://ieng6-203:1234/grade?repo=

Change or add a test to the tests file in the cloned autograder directory so that it catches the bug in the student code in the list-examples-duplicates repository.
[Ctrl C]
nano T[tab].j[tab]
  - which is nano TestListExamples.java
In the first test, change the last element of right from "h" to "e", and change the last element of expected from "h" to "e".
[Ctrl O][Enter][Ctrl X]

Show the result of running the updated grader on the list-examples-duplicates. It should show a score of 4/5 (if you added a test) or 3/4 (if you changed a test).
[up][up][Enter]
  - which java GradeServer 1234
Reload the page.

Show the result of running your updated grader on the following correct implementation. It should show a score of 5/5 (if you added a test) or 4/4 (if you changed a test). https://github.com/ucsd-cse15l-w23/list-methods-corrected
[Ctrl C]
[up][Enter]
  - which is java GradeServer 1234
Change url in browser to "corrected" and reload the page.

Show the result of running your updated grader on this repository: 
https://github.com/ucsd-cse15l-w23/list-methods-nested. It should fail reporting that ListExamples.java does not exist.
[Ctrl C]
[up][Enter]
   - which is java GradeServer 1234
Change url in browser to "nested" and reload the page.

Fix grade.sh so that instead of erroring when ListExamples.java doesn't exist in the main directory of the student solution, it searches for ListExamples.java anywhere in their submission and copies it from where it is found to the working directory of the bash script.
[Ctrl C]
nano g[tab]
  - which is nano grade.sh
Change the lines after echo (until if) to:
find . -name ListExamples.java > find-result.txt
A=`head -1 find-result.txt`
B=`wc -l < find-result.txt`
if [[ $B -gt 0 ]]
Change the cp command after the entire if structure to:
cp $A ./
[Ctrl O][Enter][Ctrl X]

Show the result of running your fixed grader on the list-methods-nested repository, where it should report that all tests pass.
[up][up][Enter]
   - which is java GradeServer 1234
Reload the page.

Show the result of running your fixed grader on list-methods-corrected repository as well, to make sure it still reports that all tests pass.
Change url in browser to "corrected" and reload the page.
