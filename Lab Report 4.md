(1) Log into ieng6  
![step 1](https://raw.githubusercontent.com/nselvakumar25/cse15l-lab-reports/main/step1-lab4.png)  
~~~
ssh cs15lfa23of@ieng6.ucsd.edu <enter> - this command logs into ieng6
~~~
(2) Clone your fork of the repository from your Github account (using the SSH URL)  
![step 2](https://raw.githubusercontent.com/nselvakumar25/cse15l-lab-reports/main/step2-lab4.png)  
~~~
Click on the green Code button on Github and copy the SSH url
git clone git@github.com:nselvakumar25/lab7.git <enter> - clones the repository so that it creates a lab7 directory in ieng6
~~~
(3) Run the tests, demonstrating that they fail  
![step 3](https://raw.githubusercontent.com/nselvakumar25/cse15l-lab-reports/main/step3-lab4.png)  
~~~
cd lab7 <enter> - changes directories from the home directory to the lab7 directory
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java <enter> - 
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests <enter>
the two commands above compile and run JUnit and all the java files in the lab7 directory
~~~
(4) Edit the code file to fix the failing test  
![step 4](https://raw.githubusercontent.com/nselvakumar25/cse15l-lab-reports/main/step4-lab4.png)  
~~~
vim ListExamples.java - opens the ListExamples.java file with vim in order to edit it
:44 <enter> - jumps to line 44 because that is the line that must be edited
<l> <l> <l> <l> <l> - moves five times to the left starting at the beginning of line 44 until the cursor is on the value that must be changed (1)
<x> - deletes 1 in index1
<i> - enters insert mode
<2> - adds 2 where the 1 in index1 used to be
<escape> - exits insert mode
:wq <enter> - saves the changes that were made and quits vim
~~~
(5) Run the tests, demonstrating that they now succeed  
![step 5](https://raw.githubusercontent.com/nselvakumar25/cse15l-lab-reports/main/step5-lab4.png)  
~~~
<up> <up> <up> <enter> - the javac -cp command was run 3 commands above in the search history so the up arrows navigate to it and enter runs it 
<up> <up> <enter> - the java -cp command was run 3 commands above in the search history so the up arrows navigate to it and enter runs it 
~~~
(6) Commit and push the resulting change to your Github account (you can pick any commit message!)  
![step 6](https://raw.githubusercontent.com/nselvakumar25/cse15l-lab-reports/main/step6-lab4.png)  
~~~
git add ListExamples.java <enter> - stages the ListExamples.java file to be in the next commit
git commit -m "lab report 4" <enter> - creates a commit locally for all files that were stages and saves "lab report 4" as the commit message
git push <enter> - sends changes to github
~~~

