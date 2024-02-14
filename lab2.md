# Lab 3 Report

## Part 1

**ChatServer.java**

```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    String chat = "";

    public String handleRequest(URI url) {
        if(url.getPath().equals("/")) {
            return chat;
        } else {
            if(url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("&");
                String[] messageInfo = parameters[0].split("=");
                String[] userInfo = parameters[1].split("=");
                if(messageInfo[0].equals("s")&&userInfo[0].equals("user")){
                    chat = chat + userInfo[1] + ": " + messageInfo[1] + "\n";
                }
                return chat;
            }
            return "404 Not Found!";
        }
    }
}

```
```

class ChatServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0) {
            System.out.println("Missing port number! Try any number betwwen 1024 to 49151");
            return;
        }
        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}
```

|[Image](chatserver1.png)

- `handleReqest` called and public String handleRequest(URI url) method is used which is the method in the Handler class. The argument is the url request which is a string and this determines what is done by the web server. The values that are changed are the return message which adds the newly entered string ("How are you") on the url and there's an incremeted number count from the previous message and the "num" variable, which represents a counter of the number of messages added increments by 1, when "How are you" is entered.

|[Image](chatserver2.png)

- `handleReqest` called and the argument is the url request as a string which determines the action that the web server does. The changed values includes the return message which gets the string that is entered on the url as input and the variable "num" which is a counter of the number of strings added and initializes to 1 when the first message is entered through the url.

# Part 2

Private Key
[Image](key-path-private.png)

Public Key
[Image](key-path-public.png)

Terminal No Password
|[Image](no-pw.png)

# Part 3

I learned a lot about ports and how the network button on the terminal works in these labs. 
I was not familiar with port numbers and commands to not need the password to log into our account.
