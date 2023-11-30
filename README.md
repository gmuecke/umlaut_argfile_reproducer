Steps to reproduce:

1. build the project using maven `mvn package`, this will produce 
   a file `target/ümlaut_demö.jar`
2. run the demo (`demo.cmd` or `demo.sh`)

I tested with JDK 21 (latest temurin) on Windows 11.

The original problem I had was, that Intellij shortens command line
by using an argfile. As my name contains an Umlaut (Gerald Mücke), and so
does my microsoft account, my windows profile path is C:\Users\GeraldMücke
and all the classpath entries in the argfile generated by IntellJ
contain this path, rendering the argfile option totally unusable.

The error occurs, when the encoding of the argfile is UTF-8
When the encoding is ISO-8859-1 it works (on my machine)
- unfortunately this can't be controlled in intellj.
