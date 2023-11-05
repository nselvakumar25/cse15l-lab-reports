# Lab Report 2
# PART 1
**Code for StringServer.java**  
![StringServer.png](https://raw.githubusercontent.com/nselvakumar25/cse15l-lab-reports/main/StringServer.png)

**Screenshot #1**  
![StringServer.png](https://raw.githubusercontent.com/nselvakumar25/cse15l-lab-reports/main/Hello.png)  
Methods that are called: handleRequest() 
```
String str = "";
    int num = 1;

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return String.format("", str);
        } else {
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    str += String.valueOf(num) + ". "; 
                    for(int i = 1; i < parameters.length; i++){
                        str += parameters[i];
                    }
                    str += "\n";
                    num += 1;
                    return String.format("%s", str);
                }
            }
            return "404 Not Found!";
        }
    }
```
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
![StringServer.png](https://raw.githubusercontent.com/nselvakumar25/cse15l-lab-reports/main/How-are-you.png)  
Methods that are called: handleRequest()  
```
String str = "";
    int num = 1;

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return String.format("", str);
        } else {
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    str += String.valueOf(num) + ". "; 
                    for(int i = 1; i < parameters.length; i++){
                        str += parameters[i];
                    }
                    str += "\n";
                    num += 1;
                    return String.format("%s", str);
                }
            }
            return "404 Not Found!";
        }
    }
```
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

# PART 2  
Path to Private Key  
![StringServer.png](https://raw.githubusercontent.com/nselvakumar25/cse15l-lab-reports/main/ssh-key-private.png)  
Path to Public Key  
![StringServer.png](https://raw.githubusercontent.com/nselvakumar25/cse15l-lab-reports/main/ssh-key-public.png)  

Logging into ieng6 without a password
![StringServer.png](https://raw.githubusercontent.com/nselvakumar25/cse15l-lab-reports/main/login.png)

# PART 3  
In the lab from week 2, I learned how to compile .java files into .class files using the javac command. Then, I learned how to use the .class files to run a server.
