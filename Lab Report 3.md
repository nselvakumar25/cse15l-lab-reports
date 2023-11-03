A failure-inducing input for the buggy program, as a JUnit test 
```
@Test
    public void testFilterFail() {
        List<String> input = new ArrayList<String>();
        input.add("a");
        input.add("b");
        input.add("c");
        StringChecker sc = new StringCheck();

        List<String> actualOutput = ListExamples.filter(input, sc);

        List<String> expectedOutput = new ArrayList<String>();
        expectedOutput.add("a");
        expectedOutput.add("b");

        assertEquals(expectedOutput, actualOutput);
    }
```

An input that doesn’t induce a failure, as a JUnit test
```
@Test
    public void testFilterSuccess() {
        List<String> input = new ArrayList<String>();
        input.add("a");
        input.add("a");
        StringChecker sc = new StringCheck();

        List<String> actualOutput = ListExamples.filter(input, sc);

        List<String> expectedOutput = new ArrayList<String>();
        expectedOutput.add("a");
        expectedOutput.add("a");

        assertEquals(expectedOutput, actualOutput);
    }
```

The symptom, as the output of running the tests  
![output of running tests](https://raw.githubusercontent.com/nselvakumar25/cse15l-lab-reports/main/test-output-lab3.png)  

The bug, as the before-and-after code change required to fix it  



