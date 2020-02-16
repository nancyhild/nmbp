## QR Code Tutorial

This tutorial explains the [qrcode demo](https://github.com/nimbella/demo-projects/tree/master/qrcode)  available on GitHub.

The demo has the following code and configuration components:

- A  single index.html file that provides a field for a visitor to enter some text and click **Submit** to generate a corresponding QR code.
- A single JavaScript file that provides the logic for the conversion of text to QR code.
- A project configuration file called *package.json*, which triggers a build of the *qr* action when it is placed in the *packages/default/qr* directory.

   See the section on [incorporating build steps](LINK) in the *Nimbella Command Line Tool* document.

### Project file structure

The GitHub project is set up with the file structure that Nimbella uses to intelligently deploy the project:

![](assets/qrcodetutorial-11520868.svg)

Here are the basics of the file structure of this project.

- The *packages* directory contains the project's actions. The first subdirectory name usually serves as the package qualifier, but when it's named *default*, no qualifier is prepanded to the action name. The next subdiretory, *qr*, is the name of the action, and the *qr.js* file contains the logic for that action.
- The *web* directory contains the static web content for the project. In this case, there is just one HTML file and one image.

### Notes on QR logic

\[\[NH: Does qr.js contain any code that would be different from the usual JavaScript that you'd write for  a web page?]]

### Notes on QR web content

The index.html file contains the usual markup and logic that you'd write for standard web deployment. In this case, it calls the qr.js logic to apply the logic to the form input.

\[\[NH: Anything else helpful to say about the HTML file contents?]]

### Notes on packages.json
\[\[NH: Anything  helpful to say about the build file contents? They might be seeing this doc before they see the nim guide, so do you want to put some basic explanation here?]]

### Deploy this project

**To deploy the qr project:**
1. Use the `md` command to navigate to the qr project on your local system.
2. Run the following line in nim:

   `deploy project qr`

   **Note:** If your package has a qualifier other than `default`, prepend the qualifier into the command. For example if the `default` directory were named `demo`, the command would be `deploy project demo/qr`.
