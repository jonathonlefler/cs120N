# Windows Setup instuctions for CS120 using Eclipse 2019-03 (4.11), Windows 10, jdk11, and javafx11

### Step 1: Check current jdk version

Open the "Add or Remove Programs" utility, and search for "java".

If nothing appears, then move on to step 2.

If "Java(TM) SE Development Kit 11.0.3" appears, move on to step 3.

If you have a Kit of a different version, left click it and Uninstall.

  
### Step 2: Download and Install jdk11

[Go to oracle and download jdkll for windows, choose the .exe option][1]

Take note of your instaliation direcotry.

### Step 3: Verify java home path

Open a command prompt. (Search cmd in the app search bar)

Type `java -version`

It should print out something like:

```
java version "11.0.3" 2019-04-16 LTS
Java(TM) SE Runtime Environment 18.9 (build 11.0.3+12-LTS)
Java HotSpot(TM) 64-Bit Server VM 18.9 (build 11.0.3+12-LTS, mixed mode)
```
If the version is 11, move on to step 4.

If the version is not 11 refer to Step 1 uninstalaition

If nothing prints out, or you get `'java' is not recognized`:

1. Type "System" in the app search bar and open up the System app
2. Click "Advanced system settings"
3. Click "Environment Variables" in the bottom right
4. In the "System variables" box, find the viarable "Path" and left click it
5. Underneath the "System variables" box, click the "Edit..." button
6. Click the "New" button, and type the fully qualified path to your java11 instaliation.
    * It's _usually_ `C:\Program Files\Java\jdk-11.0.3\bin`
7. Click the "OK" button in the "Edit encironmental variable" dialogue box
8. Click the "OK" button in the "Environmental Variables" dialogue box
9. Click the "OK" button in the "System Properties" diaglogue box
10. Restart your computer
11. Verify `java -version` works and outputs the correct version

### Step 4: Install javafx11

[Install the javafx11 SDK][2]

Extract the .zip folder to C:\path\to\Java\jdk-11.0.3

### Step 5: Download and install Eclipse

[Download link][3]

Choose the "Eclipse IDE for Java Developers" option when prompted.

Choose defualt options for the rest of the install process. Take note of your instaliation directory.

### Step 6: Configure Eclipse

1. In the task bar, click "Windows" -> "Prefernces"
2. In the left column, select "Java" -> "Build Path" -> "User Libraries"
3. In the "User Libraries" menu, click the "New..." button
4. Input "javafx11" for the "User library name"
5. Left click the newely created library and slect the "Add External JARs..." button
6. Navigate to your javafx11 install directory and go into the `lib` directory
7. Select all of the executable jar files
    * All files should be selected except the `src.zip` folder
8. Click the "Open" button
9. Click the "Apply and Close" button

## Setup Done!

# Creating a Basic javafx Application

1. Create a new java project
    * Be sure to use the jdk11 jre
    * Don't create module.info
2. Right click the project folder, and select "Properties"
3. Select "Java Build Path"
4. In the "Java Build Path" menu, left click "Modulepath" and select the "Add Library..." button
5. Select "User Library" and click the "Next >" button
6. Check the javafx11 library you created and click the "Finish" button
7. Click the "Apply and Close" button
8. In the taskbar, click "Run" -> "Run Configurations..."
9. Navigate to the "Arguments" tab
10. In "VM arguments:" box, input:
    * `--module-path "\path\to\javafx-sdk-11.0.3\lib" --add-modules javafx.controls,javafx.fxml`
    * Be sure the path to your jdk11 is correct!
11. Click the "Close" button

## Creation Done!

  [1]: https://www.oracle.com/technetwork/java/javase/downloads/jdk11-downloads-5066655.html
  [2]: https://gluonhq.com/products/javafx/
  [3]: https://www.eclipse.org/downloads/
