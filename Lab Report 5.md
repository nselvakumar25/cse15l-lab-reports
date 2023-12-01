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
File and Directory Structure:  
lab-report-5-cse15l  
    lib  
        hamcrest-core-1.3.jar  
        junit-4.13.2.jar  
    .gitignore  
    ListExamples.java  
    ListExamplesTests.java  
    test.sh  

Contents of ListExamples.java  
~~~
import java.util.ArrayList;
import java.util.List;

interface StringChecker {
  boolean checkString(String s);
}

class StringCheck implements StringChecker {
  public boolean checkString(String s) {
    return s.equals("a");
  }
}

class ListExamples {

  // Returns a new list that has all the elements of the input list for which
  // the StringChecker returns true, and not the elements that return false, in
  // the same order they appeared in the input list;
  static List<String> filter(List<String> list, StringChecker sc) {
    List<String> result = new ArrayList<>();
    for (String s : list) {
      if (sc.checkString(s)) {
        list.add(s);
      }
    }
    return result;
  }
}
~~~

Contents of ListExamplesTests.java
~~~
import static org.junit.Assert.*;
import org.junit.*;
import java.util.*;
import java.util.ArrayList;

public class ListExamplesTests {
	@Test
	public void testFilter() {
		List<String> input = new ArrayList<String>();
		input.add("a");
		input.add("a");
		input.add("b");
		StringChecker sc = new StringCheck();
		List<String> actualOutput = ListExamples.filter(input, sc);
		List<String> output = new ArrayList<String>();
		output.add("a");
		output.add("a");
		assertEquals(actualOutput, output);
	}
}
~~~

Contents of test.sh  
~~~
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests
~~~
