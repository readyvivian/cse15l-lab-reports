# Week 3 Lab Report

Vivian Wang | A17457779 |v8wang@ucsd.edu

## Part 1

Code for `StringSever`:

```java
import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;

class SearchHandler implements URLHandler {

    ArrayList<String> strings = new ArrayList<>();

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return displayStrings();
        }
        else if (url.getPath().contains("/add-message")) {
            String[] temp = url.getQuery().split("=");
            if (temp[0].equals("s")) {
                strings.add(temp[1]);
                return displayStrings();
            }
        }
        return "404 Not Found!";
    }

    private String displayStrings() {
        String output = "";
        if (strings.size() > 0) {
            output = strings.get(0);
            for (int i = 1; i < strings.size(); i++) {
                output += "\n" + strings.get(i);
            }
        }
        return output;
    }
}

class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new SearchHandler());
    }
}
```

Screenshots for using `/add-message`:

![week1-part1-1](lab-report-images/week3-part1-1.png)

The`handleRequest` method in `SearchHandler` and the `displayStrings` method in `SearchHandler` are called.

The relevant arguments are the arguments under `else if (url.getPath().contains("/add-message"))`  and all the arguments in the `displayStrings` method.

The `URI url` changes to `http://localhost:7012/add-message?s=Hello`, the `String[] temp` changes to `[s, Hello]`, the `ArrayList<String> strings` changes to `[Hello]`, the `String output` changes to `Hello`.

![week1-part1-1](lab-report-images/week3-part1-2.png)

The`handleRequest` method in `SearchHandler` and the `displayStrings` method in `SearchHandler` are called.

The relevant arguments are the arguments under `else if (url.getPath().contains("/add-message"))`  and all the arguments in the `displayStrings` method.

The `URI url` changes to `http://localhost:7012/add-message?s=How are you`, the `String[] temp` changes to `[s, How are you]`, the `ArrayList<String> strings` changes to `[Hello, How are you]`, the `String output` changes to `Hello \n How are you`.

## Part 2

h

## Part 3

This is the first time a learned about web server and git. 