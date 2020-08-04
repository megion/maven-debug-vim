# maven java project for testing debugging in vim

Instructions:

- set debug port in file `.vimspector.json` via prop `configuration.Java Attach.configuration.port` (for exemple 5006).
- `mvn clean compile`
- `cd target/classes/`
- `java -cp . -Xrunjdwp:transport=dt_socket,address=5006,server=y,suspend=y com.vimspector.test.TestApplication`
- in vim, open `src/main/java/com/vimspector/test/TestApplication.java`
- set a breakpoint on main `F9` [see keys map](https://github.com/puremourning/vimspector#human-mode) 
- start the debug session in Vim by hitting the `F1` key 

Another example debugging tests for maven project [remote debugging Maven tests](https://maven.apache.org/surefire/maven-surefire-plugin/examples/debugging.html)
