ZoK;BoMiFuYaSeWuRa@oDaSoVoPiZo


ssh cs15lwi23agc@ieng6.ucsd.edu


git clone https://github.com/ucsd-cse15l-w23/skill-demo1-server


cd skill-demo1-server

javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java

java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore FileServerTests

(find junit command in week 3 setup)


git clone https://github.com/ucsd-cse15l-w23/skill-demo1-data


find skill-demo1-data/ > find-results.txt

grep ".txt" find-results.txt > grep-results.txt

wc -l grep-results.txt


grep -l "Lucayans" `find skill-demo1-data/ -name "*.txt"`


java FileServer 7123 skill-demo1-data

http://ieng6-202.ucsd.edu:7123


http://ieng6-202.ucsd.edu:7123/search?q=Bahamas-History


http://ieng6-202.ucsd.edu:7123/search?q=IntroL
