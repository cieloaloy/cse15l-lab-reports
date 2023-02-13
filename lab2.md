# Lab Report 2

This tutorial contains instructions on how to run a simple server containing a string as well as testing for bugs using JUnit.



## Part 1: StringServer

The StringServer contains a single string that gets appended to by the user. As the user inputs new requests such as the following,
```
/add-message?s=Hello
```
the server appends "Hello" to the string and prints the current contents.

Here is an example code for the StringServer:

```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
    String running = "";

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return String.format(running);
        } else {
            System.out.println("Path: " + url.getPath());
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("=");
                running = running + " " + parameters[1] + "\n";
                return String.format(running);
            }
            return "404 Not Found!";
        }
    }
}

class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}
```

Using the code above, we can use the `/add-message` path as follows.

(image)

(image)




## Part 2: Addressing Bugs






## Part 3: Summary of Knowledge
