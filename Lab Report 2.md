**Code for StringServer.java**  
![StringServer.png](/github.com/nselvakumar25/cse15l-lab-reports/StringServer.png)

**Screenshot #1**  
![StringServer.png](/github.com/nselvakumar25/cse15l-lab-reports/Hello.png)  
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
![StringServer.png](/github.com/nselvakumar25/cse15l-lab-reports/How-are-you.png)  
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
