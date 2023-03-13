ssh

\\\\\

git clone

\\\\\

cd g[tab]
javac *Server.java
java GradeServer 1234

\\\\\

In browser:
http://ieng6-203:1234/grade?repo=

\\\\\

[Ctrl C]
nano T[tab].j[tab]
  -which is nano TestListExamples.java
In the first test, change the last element of right from "h" to "e", and change the last element of expected from "h" to "e".
[Ctrl O][Enter][Ctrl X]

\\\\\

[up][up][Enter]
  -which java GradeServer 1234
Reload the page.

\\\\\

[Ctrl C]
[up][Enter]
  -which is java GradeServer 1234
Change url in browser to "corrected" and reload the page.

\\\\\

[Ctrl C]
[up][Enter]
   -which is java GradeServer 1234
Change url in browser to "nested" and reload the page.

\\\\\

[Ctrl C]
nano g[tab]
  -which is nano grade.sh

Change the lines after echo (until if) to:
find . -name ListExamples.java > find-result.txt
A=`head -1 find-result.txt`
B=`wc -l < find-result.txt`
if [[ $B -gt 0 ]]

Change the cp command after the entire if structure to:
cp $A ./

[Ctrl O][Enter][Ctrl X]

\\\\\

[up][up][Enter]
   -which is java GradeServer 1234
Reload the page.

\\\\\

Change url in browser to "corrected" and reload the page.
