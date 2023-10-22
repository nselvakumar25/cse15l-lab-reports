#**PART 1**
**Code for StringServer.java**  
![StringServer.png]([https://github.com/nselvakumar25/cse15l-lab-reports/StringServer.png/](https://raw.githubusercontent.com/nselvakumar25/cse15l-lab-reports/main/StringServer.png))

**Screenshot #1**  
![StringServer.png](https://github.com/nselvakumar25/cse15l-lab-reports/Hello.png/)  
Methods that are called: handleRequest()  
Relevant arguments: URI url  
Value of fields before the request: 
* url = null
* str = ""
* num = 1
How the fields change from this request:
* url = /add-message?s=Hello 
* str = "1. Hello"
* num = 2

**Screenshot #2**  
![StringServer.png](https://github.com/nselvakumar25/cse15l-lab-reports/How-are-you.png/)  
Methods that are called: handleRequest()  
Relevant arguments: URI url  
Value of fields before the request: 
* url = /add-message?s=Hello 
* str = "1. Hello"
* num = 2
How the fields change from this request:
* url = /add-message?s=How%20are%20you
* str = "1. Hello"
         2. How are you"
* num = 3

#**PART 2**
![StringServer.png](/github.com/nselvakumar25/cse15l-lab-reports/ssh-key.png)  
![StringServer.png](/github.com/nselvakumar25/cse15l-lab-reports/login.png)  

#**PART 3**  
In the lab from week 2, I learned how to compile .java files into .class files using the javac command. Then, I learned how to use the .class files to run a server.
