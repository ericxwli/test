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
* In the Run menu, choose `Run` or `Debug`, and choose `gngrDev` as the launch configuration.

### Testing
The `file://` protocol is disabled in `gngr` as of now, for security reasons. To load an `html` file from your local system, you can start a server locally, and access through `http`.

A simple server can be quickly started with this command: `python -m SimpleHTTPServer`. It serves files from the current directory. A better performing server can be started with the help of [this script](https://gist.github.com/hrj/c91b46b3e4bba091fef5).

### Coding
We need to follow a consistent coding style and format so that the code is readable to everyone
and there are fewer differences between commits.

Eclipse has an auto-formatting feature (Menu: `Source/Format`) but we first need to configure it.
The settings used by us are exported to a file in the repo, and you need to import them into your
Eclipse.

#### How to import the Code Formatter settings
* Go to `Window > Preferences > Java > Code Style > Formatter` and click `Import...`
* Select the file `misc/EclipseJavaFormat_Spaced.xml` from the repository.

### Tips for using git & github

* Commit messages: Some good tips [here](https://github.com/erlang/otp/wiki/Writing-good-commit-messages) to begin with, but need to adapt a little bit.
* Rebasing pull requests: [Pretty detailed guide]