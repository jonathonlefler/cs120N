# Windows Setup instuctions for CS120 using Eclipse 2019-03 (4.11), Windows 10, jdk11, and javafx11

### Step 1: Check current jdk version

Open the "Add or Remove Programs" utility, and search for "java".

If nothing appears, then move on to step 2.

If "Java(TM) SE Development Kit 11.0.3" appears, move on to step 3.

If you have a Kit of a different version, left click it and Uninstall.

  
### Step 2: Download and Install jdk11

[Go to oracle and download jdkll for windows, choose the .exe option][1]

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

Otherwise if the version is not 11, nothing prints out, or you get `'java' is not recognized`:

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

  [1]: https://www.oracle.com/technetwork/java/javase/downloads/jdk11-downloads-5066655.html
