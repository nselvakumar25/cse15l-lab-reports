Hello, I keep getting this error when I try to run the tests on ListExamples.java. Since it's throwing a ConcurrentModificationException, I'm assuming it means something is being changed while to for loop is running but I'm not sure how to fix this.
![part 1](https://raw.githubusercontent.com/nselvakumar25/cse15l-lab-reports/main/lab5-p1.png)  

Hey, I recommend trying to see which ArrayList variable is actually being altered. Check this using jdb and seeing the values of each variable on a given line.

Screenshot of student figuring out the bug using the TA's advice
![part 2](https://raw.githubusercontent.com/nselvakumar25/cse15l-lab-reports/main/lab5-p2.png)  

