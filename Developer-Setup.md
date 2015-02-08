### Pre-requisites
* JDK, version 8+
* Eclipse Luna or newer

### Building
* `git clone` the repo
* In Eclipse, import the projects into your workspace. You need to navigate to the `src/` folder in the cloned repository and import all projects recursively.
* There should be no compilation errors at this stage.

### How to Run or Debug gngr in Eclipse
#### Importing the Launch Configuration
This needs to be done only once.
* In Eclipse File menu, select Import -> `Run/Debug` -> `Launch Configuration`
* Pick the `gngr/misc/` folder (from the cloned repo)
* Pick the `gngrDev` launch configuration and click `Finish`.

#### Launching
* In Eclipse / Package Explorer click the `Platform_Core` project and ensure it is selected.
* In the Run menu, choose `Run` or `Debug`, and choose `gngr` as the launch configuration.