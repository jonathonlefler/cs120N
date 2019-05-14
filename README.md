setup for javafx11, jdk11, and eclipse on ubuntu 18.04

Install openjdk11 and javafx11
`sudo apt install openjdk-11-jdk openjfx`
https://gluonhq.com/products/javafx/

check java -version reads out the correct jdk version

install the newest eclipse 2019-03 (4.11)
https://www.eclipse.org/downloads/

Choose java dev for EE

When creating a project:
1. ___dont create module.info___
2. Create a new user library:
  - name it javafx
  - include all of the jars in /path/to/javafx/lib
3. add libary to module path
4. in run config, add this to VM arguments: `--module-path /usr/lib/jvm/javafx-sdk-11.0.2/lib --add-modules javafx.controls,javafx.fxml`
