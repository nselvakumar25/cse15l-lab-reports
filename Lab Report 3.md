# Lab Report 3
## PART 1
**A failure-inducing input for the buggy program, as a JUnit test**
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

**An input that doesn’t induce a failure, as a JUnit test**
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

**The symptom, as the output of running the tests** 
![output of running tests](https://raw.githubusercontent.com/nselvakumar25/cse15l-lab-reports/main/test-output-lab3.png)  

**The bug, as the before-and-after code change required to fix it**  

## PART 2
**Command-line option 1: grep -m num**  
example 1:
```
(base) Nishithas-MacBook-Air:Alcohol_Problems nishi$ grep -m 3 alcohol Session3-PDF.txt
Excessive alcohol consumption plays an important role in many of
documented the presence of alcohol among patients admitted to
studies have demonstrated that even blood alcohol concentration
```
example 2:
```
(base) Nishithas-MacBook-Air:Alcohol_Problems nishi$ grep -m 3 treatment Session4-PDF.txt
unaware of their need for treatment. The provision of alcohol
these patients are unlikely to present for treatment on their
How-ever, motivation can facilitate treatment. Studies suggest that
```
What it's doing and why it's useful:  
Source: man grep  

**Command-line option 2: grep -L**  
example 1:
```
(base) Nishithas-MacBook-Air:docsearch nishi$ grep -L "helloo" technical/911report/*.txt
technical/911report/chapter-1.txt
technical/911report/chapter-10.txt
technical/911report/chapter-11.txt
technical/911report/chapter-12.txt
technical/911report/chapter-13.1.txt
technical/911report/chapter-13.2.txt
technical/911report/chapter-13.3.txt
technical/911report/chapter-13.4.txt
technical/911report/chapter-13.5.txt
technical/911report/chapter-2.txt
technical/911report/chapter-3.txt
technical/911report/chapter-5.txt
technical/911report/chapter-6.txt
technical/911report/chapter-7.txt
technical/911report/chapter-8.txt
technical/911report/chapter-9.txt
technical/911report/preface.txt
```
example 2:
```
(base) Nishithas-MacBook-Air:docsearch nishi$ grep -L "environment" technical/government/Env_Prot_Agen/*.txt
technical/government/Env_Prot_Agen/ctf7-10.txt
```
What it's doing and why it's useful:  
Source: man grep  

**Command-line option 3: grep -B num**  
example 1:
```
(base) Nishithas-MacBook-Air:docsearch nishi$ grep -L "environment" technical/government/Env_Prot_Agen/*.txt
technical/government/Env_Prot_Agen/ctf7-10.txt
(base) Nishithas-MacBook-Air:docsearch nishi$ man grep
(base) Nishithas-MacBook-Air:docsearch nishi$ grep -B 2 "Earth" technical/government/Env_Prot_Agen/*.txt
technical/government/Env_Prot_Agen/final.txt-SO2 and NOx. Acidic deposition or "acid rain" occurs when SO2 and
technical/government/Env_Prot_Agen/final.txt-NOx in the atmosphere react with water, oxygen, and oxidants to
technical/government/Env_Prot_Agen/final.txt:form acidic compounds. These compounds fall to the Earth in either
--
technical/government/Env_Prot_Agen/final.txt-up-to-date information about what is known and about what is not
technical/government/Env_Prot_Agen/final.txt-known on the science of climate change.
technical/government/Env_Prot_Agen/final.txt:We know the surface temperature of the Earth is warming. It has
--
technical/government/Env_Prot_Agen/final.txt-to the 1970s, and then sharply rising temperatures from the 1970s
technical/government/Env_Prot_Agen/final.txt-to today. There is a natural greenhouse effect that contributes to
technical/government/Env_Prot_Agen/final.txt:warming. Greenhouse gases trap heat and thus warm the Earth because
```
example 2:
```
(base) Nishithas-MacBook-Air:docsearch nishi$ grep -B 1 "Charles Darwin" technical/plos/*.txt
technical/plos/journal.pbio.0020046.txt-        Winston Churchill had to rehearse all his public speeches to perfection and even practiced
technical/plos/journal.pbio.0020046.txt:        answers to possible questions and criticisms to avoid stuttering. Charles Darwin also
--
technical/plos/journal.pbio.0020311.txt-        from a classical experiment on phototropism, the bending of plants toward light, carried
technical/plos/journal.pbio.0020311.txt:        out by Charles Darwin and his son Francis in 1880. The Darwins were able to demonstrate
--
technical/plos/journal.pbio.0020347.txt-        ancestral species through the process of hybridization and selection as originally
technical/plos/journal.pbio.0020347.txt:        described by Charles Darwin (1859).
--
technical/plos/journal.pbio.0020439.txt-        opening the head, by using the Radon transform to infer the densities of materials at each
technical/plos/journal.pbio.0020439.txt:        location within the head (Hsieh 2003). Charles Darwin was right when he wrote that people
```
What it's doing and why it's useful:  
Source: man grep  

**Command-line option 4: grep -n**  
example 1:
```
(base) Nishithas-MacBook-Air:docsearch nishi$ grep -n "Earth" technical/government/Env_Prot_Agen/*.txt
technical/government/Env_Prot_Agen/final.txt:392:form acidic compounds. These compounds fall to the Earth in either
technical/government/Env_Prot_Agen/final.txt:505:We know the surface temperature of the Earth is warming. It has
technical/government/Env_Prot_Agen/final.txt:510:warming. Greenhouse gases trap heat and thus warm the Earth because
```
example 2:
```
(base) Nishithas-MacBook-Air:docsearch nishi$ grep -n "biomedical data" technical/biomed/*.txt
technical/biomed/1472-6882-3-3.txt:49:        Other biomedical databases that include CAM literature,
technical/biomed/1472-6947-3-5.txt:49:        another level of biomedical data integration in which array
technical/biomed/1472-6947-3-8.txt:56:          Creators of biomedical databases use terminologies to
technical/biomed/1472-6947-3-8.txt:624:        biomedical data sets. Public comment is welcomed.
```
What it's doing and why it's useful:  
Source: man grep







