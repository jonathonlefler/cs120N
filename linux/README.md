# Setup for javafx11, jdk11, and Eclipse on Ubuntu 18.04

### Step 1: Install openjdk11 and javafx11 SDK

> `sudo apt install openjdk-11-jdk openjfx`

Be sure to select the SDK version of javafx!

> [javafx](1)


### Step 2: Check java Version Reads Out the Correct jdk Version

> `java -version`

The output should look like this:

```none
openjdk version "11.0.3" 2019-04-16
OpenJDK Runtime Environment (build 11.0.3+7-Ubuntu-1ubuntu218.04.1)
OpenJDK 64-Bit Server VM (build 11.0.3+7-Ubuntu-1ubuntu218.04.1, mixed mode, sharing)
```

### Step 3: Install the Newest Eclipse 2019-03 (4.11)

> [Download link](2)

Choose java dev, the top option

### Step 4: Setup Eclipse for javafx

1. In the task bar, click "Windows" -> "Prefernces"
2. In the left column, select "Java" -> "Build Path" -> "User Libraries"
3. In the "User Libraries" menu, click the "New..." button
4. Input "javafx11" for the "User library name"
5. Left click the newely created library and slect the "Add External JARs..." button
6. Navigate to your javafx11 install directory and go into the `lib` directory
7. Select all of the .jar files
    * All files should be selected except the `src.zip` folder
8. Click the "Open" button
9. Click the "Apply and Close" button

## Steup Done!

### When creating a project:
1. Create a new java project
    * Be sure the jdk used for the project is jdk11
    * ___Don't create module.info___
2. Right click your project folder and click "Properties". Go to the "Libraries" Tab and left click "Module Path". On the right, select "Add Library" and choose "User Library"
3. Check the javafx11 library you created and click the "Finish" button
4. In run configuration, found in the run taskbar, select the "Arguments" tab and add this to VM arguments:
      * `--module-path /usr/lib/jvm/javafx-sdk-11.0.2/lib --add-modules javafx.controls,javafx.fxml`
      * Be sure the path to your javafx is correct!

## Creation Done!

[1]:https://gluonhq.com/products/javafx/
[2]:https://www.eclipse.org/downloads/
