### Setup for javafx11, jdk11, and Eclipse on Ubuntu 18.04

Install openjdk11 and javafx11

`sudo apt install openjdk-11-jdk openjfx`
https://gluonhq.com/products/javafx/

check java -version reads out the correct jdk version

install the newest eclipse 2019-03 (4.11)
https://www.eclipse.org/downloads/

Choose java dev for EE

When creating a project:
1. Create a new java project
    * Be sure the jdk used for the project is jdk11
    * ___dont create module.info___
2. Right click your project folder and click "Properties". Go to the "Libraries" Tab and left click "Module Path". On the right, select "Add Library" and choose "User Library"
    * name it javafx
    * include all of the jars in /path/to/javafx/lib
3. Add the newely created libary to the projects module path
4. In run configuration, found in the run taskbar, select the "Arguments" tab and add this to VM arguments: `--module-path /usr/lib/jvm/javafx-sdk-11.0.2/lib --add-modules javafx.controls,javafx.fxml`
