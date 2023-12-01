# Lab Report 4  

**Student's Post:**  
Hello, I keep getting this error when I try to run the tests on ListExamples.java. Since it's throwing a ConcurrentModificationException, I'm assuming it means something is being changed while the for loop is running but I'm not sure how to fix this.
![part 1](https://raw.githubusercontent.com/nselvakumar25/cse15l-lab-reports/main/lab5-p1.png)  

**TA's Response:**  
Hey, I recommend trying to see which ArrayList variable is actually being altered. Check this using jdb and seeing the values of each variable on a given line.

Screenshot of student figuring out the bug using the TA's advice:
![part 2](https://raw.githubusercontent.com/nselvakumar25/cse15l-lab-reports/main/lab5-p2.png)  
This shows that the list array has all the elements it should have but the result array is not having any elements added to it. Looking back at the code, we can see that this is because, in the for loop of the filter method, we are adding values to the variable list rather than the variable result. Not only does this lead to incorrect output, but it also creates an error. This error is created because the for loop is traversing the list variable but list is being changed during the traversal proces.  
To fix the bug, we can change list.add(s) to result.add(s) in the for loop.  

**Setup:**  


