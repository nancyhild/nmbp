## Overview

### Welcome to the Nimbella Cloud platform

Blurb about Nimbella platform... (integrated CDN for static web assets, functions, and state)
s

### Organization of this document

The purpose of this document is to show you by example how to create a nimbella project and use the main platform features to build a stateful cloud application. We'll use a set of tutorials to give you a feel for the various types of projects you can create.

The examples used in this document are available on GitHub in these tutorials and the Nimbella platform has integrations with GitHub to make it easy to deploy your projects from GitHub, as you'll see.

This document has the following sections:

- This overivew
- Set up your Nimbella project repo in GitHub
  If you don't want to use GitHub...
- Tutorials
  - A simple application with static web comtent plus a function, using the QR code example.
    [Example code](https://github.com/nimbella/demo-projects/tree/master/qrcode)
    [Result](https://qrdemo-apigcp.nimbella.io/?text=somewhere+over+the+rainbow): web page where visitor enter  text and generate a corresponding QR code
  - [A simple counter for page visits](https://github.com/nimbella/demo-projects/tree/master/visits)
    This extends the previous example by adding state and two functions.
  - [An Optical Chaacter Recognition \(OCR\) and print job serverless application]
    This is a more elaborate example using a React front end and more functions on the back end.
    [Preview](https://ocrdemo-apigcp.nimbella.io)

### Prerequisites

To understand these tutorials, the following developer skills will be helpful:
- Knowledge of JavaScript.
- xxx

To run these tutorials yourself, you'll need the following:
- A Nimbella Cloud account, set up with a namespace.
- The Nimbella Command Line Tool(LINK), called nim, installed on Windows or Mac.

To configure your Nimbella Cloud account and install nim, see [How To Use the Nimbella Command Line Tool](LINK).

### How to run the GitHub demos

Besides the Nimbella GitHub demos used as tutorials in thie guide, there are other demos that are also available at the [nimbella/demo-projects repository](https://github.com/nimbella/demo-projects) on  GitHub.

To see any demo project running in the cloud, deploy the project directly from your local Github directory:

1. Use cd within nim to navigate to ththe GitHub demo directory.
2. In nim, enter the following command:
   `project deploy [project-name]`
