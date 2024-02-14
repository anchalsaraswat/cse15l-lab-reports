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

- `handleReqest` called and the url is the argument
- `chat` is updated from empty by concatenating string

|[Image](chatserver2.png)

- `handleReqest` called and the url is the argument
- `chat` is updated by concatenating string


# Part 2

Private Key
|[Image](key-path-private.png)

Public Key
|[Image](key-path-public.png)

Terminal No Password
|[Image](no-pw.png)

# Part 3

I learned a lot about ports and how the network button on the terminal works in these labs. 
I was not familiar with port numbers and commands to not need the password to log into our account.
