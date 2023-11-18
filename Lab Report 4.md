(1) Log into ieng6
  ssh cs15lfa23of@ieng6.ucsd.edu <enter>
(2) Clone your fork of the repository from your Github account (using the SSH URL)
  Click on the green Code button on Github and copy the SSH url
  git clone git@github.com:nselvakumar25/lab7.git <enter>
(3) Run the tests, demonstrating that they fail
  cd lab7 <enter>
  javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java <enter>
  java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests <enter>
(4) Edit the code file to fix the failing test
  vim ListExamples.java
  :44 <enter>
  <l> <l> <l> <l> <l> 
  <x>
  <i>
  <2> 
  <escape>
  :wq <enter>
(5) Run the tests, demonstrating that they now succeed
  <up> <up> <up> <enter>
  <up> <up> <enter>
(6) Commit and push the resulting change to your Github account (you can pick any commit message!)
  git add ListExamples.java <enter>
  git commit -m "lab report 4" <enter>
  git push <enter>
  
take a screenshot, and write down exactly which keys you pressed to get to that step
summarize the commands you ran and what the effect of those keypresses were

