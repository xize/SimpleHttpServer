<h1>SimpleHttpServer</h1>

this is my first web server library written in java be aware that the library still lacks some features.

javadocs can be found at: https://0c3.eu/job/SimpleServer/

#current features:
- post support
- get support
- mime support (limited as of yet)

#how to setup a server:
```
String servername = "my-server";
SimpleServer server = new SimpleServer(servername, 80);
server.addListener(new SomeServerEvent()); //whereas SomeServerEvent implements ServerListener and has atleast one method using the @ServerEvent anotation
server.start();
```

#how to setup events:

```
public class SomeServerEvent implements ServerListener {
     @ServerEvent
     public void onEvent(SimpleServerEvent e) {
        //do something, note that you need manual register this class with server.addListener(this class); as mentoid the example above.
     }
}
```
