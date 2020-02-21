## QR Code Tutorial

This tutorial explains the [QR Code demo](https://github.com/nimbella/demo-projects/tree/master/qrcode)  available on GitHub and shows you how to deploy it to the Nimbella Cloud.

The QR Code demo is a single-page web application that generates a [QR code](https://en.wikipedia.org/wiki/QR_code) from text that a user submits. The demo has the following code and configuration components:

- A  single index.html file, which has a field for a visitor to enter some text and click **Submit**.
- A single JavaScript file that provides the backend logic for the conversion of text to QR code.
- A Node package manager file called *packages.json*, which describes what dependencies the function has.

### Project file structure

The GitHub project has the file structure that Nimbella uses to intelligently deploy the project:

![](assets/qrcodetutorial-11520868.svg)

Here are the basics of the file structure of this project.

- The *packages* directory contains the project's actions, and in this example there's only one. The first subdirectory name usually serves as the package qualifier, but when it's named *default*, no qualifier is prepanded to the action name. The next subdiretory, *qr*, is the name of the action, and the *qr.js* file contains the logic for that action.

- The *web* directory contains the static web content for the project. In this case, there is just one HTML file and one image.

### Notes on QR logic

The code for the QR action is standard Node.js. It uses an existing Node [library](https://www.npmjs.com/package/qrcode) for the actual code generation.

### Notes on QR web content

The *index.html* file contains the usual markup and logic that you'd write for standard web deployment, with an input form for text. In this case, it calls an API to retrieve a QR code for the form input. This API is implemented by *qr.js*.

### Notes on packages.json
The *packages.json* file in the *qr* directory triggers an automatic build of the action when the *qr.js* file is modified. For more information about builds, see the [section on incorporating build steps in the Nimbella Command Line Tool document](https://nimbella.io/downloads/nim/nim.html#incorporating-build-steps-for-actions-and-web-content).

### Deploy this project to the Nimbella Cloud
If you have the [Nimbella command line tool called `nim`](https://nimbella.io/downloads/nim/nim.html#install-the-nimbella-command-line-tool-nim) installed, you can deploy this project directly from GitHub.

- Run the following command in your terminal:

   `nim project deploy /path/to/qrcode`

   **Note:** If you clone the GitHub repository locally to your disk, then you can deploy from your local path. For example if you cloned the demo to */path/to/demos/qrcode* then the command would be:

   `nim project deploy /path/to/demos/qrcode`
