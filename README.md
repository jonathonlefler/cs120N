### Setup for javafx11, jdk11, and Eclipse on Ubuntu 18.04

Install openjdk11 and javafx11 SDK

> `sudo apt install openjdk-11-jdk openjfx`

Be sure to select the SDK version of javafx!

> [javafx](1)


### Check java Version Reads Out the Correct jdk Version

> `java -version`

The output should look like this:

```none
openjdk version "11.0.3" 2019-04-16
OpenJDK Runtime Environment (build 11.0.3+7-Ubuntu-1ubuntu218.04.1)
OpenJDK 64-Bit Server VM (build 11.0.3+7-Ubuntu-1ubuntu218.04.1, mixed mode, sharing)
```

### Install the Newest Eclipse 2019-03 (4.11)

> [Download link](2)

Choose java dev for EE

### When creating a project:
1. Create a new java project
    * Be sure the jdk used for the project is jdk11
    * ___Don't create module.info___
2. Right click your project folder and click "Properties". Go to the "Libraries" Tab and left click "Module Path". On the right, select "Add Library" and choose "User Library"
    * name it javafx
    * include all of the jars in /path/to/javafx/lib
         * Don't include the .src folder!
3. Add the newely created libary to the projects module path
4. In run configuration, found in the run taskbar, select the "Arguments" tab and add this to VM arguments:
      * `--module-path /usr/lib/jvm/javafx-sdk-11.0.2/lib --add-modules javafx.controls,javafx.fxml`
      * Be sure the path to your javafx is correct!

[1]:https://gluonhq.com/products/javafx/
[2]:https://www.eclipse.org/downloads/
