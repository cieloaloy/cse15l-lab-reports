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

![apples](https://user-images.githubusercontent.com/122492228/218616855-4bd7f820-6a41-4c6e-b07e-6bf2b5cd1299.png)

Within the `handleRequest` method, adding the message "Apples" consists of parsing the String parameters in the URI. Once the program determines that "add-message" is the path, it can take in the query in the String array `parameters`, splitting the content before and after the equal sign. The String  `running` continues to be changed and added to with every new request.

![blueberries](https://user-images.githubusercontent.com/122492228/218616881-93b0e219-2520-4bb0-b909-edd5eb87f7ac.png)
   
Like with the previous example, adding this message happens within `handleRequest` by parsing the URI and extracting the message from after the equal sign. `running` now contains both "Apples" and the new "Blueberries and Blackberries", separated by newline characters.



## Part 2: Addressing Bugs

In Lab 3, we investigated and tested a LinkedList implementation, among other things. However, the code was incredibly buggy. To rectify this, we tested the code using JUnit. The following append method works, but not all of the time.

```
public void append(int value) {
    if(this.root == null) {
        this.root = new Node(value, null);
        return;
    }
    // If it's just one element, add if after that one
    Node n = this.root;
    if(n.next == null) {
        n.next = new Node(value, null);
        return;
    }
    // Otherwise, loop until the end and add at the end with a null
    while(n.next != null) {
        n = n.next;
        n.next = new Node(value, null);
    }
}
```

The following test produced a failing output.

```
@Test
public void threeNumTest() {
    LinkedList list1 = new LinkedList();
    list1.append(4);
    list1.append(1);
    list1.append(3);
    assertEquals("4 1 3 ", list1.toString());
}
```

However, this next test passed!

```
@Test
public void twoNumTest() {
    LinkedList list1 = new LinkedList();
    list1.append(4);
    list1.append(1);
    assertEquals("4 1 ", list1.toString());
}
```

Why did the first test fail? Upon reaching the third call to append, the program continued indefinitely due to the while loop infinitely checking a non-null `n.next`. Because the second test only appended twice, it never reached this infinite state.

![output](https://user-images.githubusercontent.com/122492228/218622205-1c5eff2a-f0f8-4025-b444-c7992d95a27b.png)

As the terminal output shows, the first test encountered an OutOfMemoryError, due to the faulty method continuously creating new Nodes without stopping. In order to prevent this, we had to edit the append method's third case, which would handle every attempt at appending other than the very first or second.

In the original code,

```
while(n.next != null) {
    n = n.next;
    n.next = new Node(value, null);
}
```

should be changed to...

```
while(n.next != null) {
    n = n.next;
}
n.next = new Node(value, null);
```

There we go! This new implementation passed both tests and correctly appended an item to the LinkedList. Taking the creation of `n.next` outside of the loop allowed the loop to accurately traverse to the end of the list without stalling the program.


## Part 3: Summary of Knowledge

Lab 3 greatly assisted in my understanding of running JUnit tests from the command-line instead of the built-in way using VS Code. It is really helpful and clear to see a list of the failed tests and which lines caused errors without additional bits and bobs strewn on, like it would show when using the IDE's debugger.
