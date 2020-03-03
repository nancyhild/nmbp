## Page Visit Counter Tutorial

This tutorial describes the [Visits demo](https://github.com/nimbella/demo-projects/tree/master/visits) and shows you how to deploy it to the Nimbella Cloud.

The Visits app is stateful and displays on a web page how many times the page has been uniquely visited since the project was deployed. You can [view the app here](LINK).

This project has the following components:

- A web front end with a single HTML file.
- Two functions in the back end, implemented with PHP, which create and manage the cookie for the app, and increment the data store of the visit count.

### Project file structure

The GitHub project has the file structure that Nimbella uses to deploy the project with minimal configuration. Here is the directory structure for the Visits project:

![](assets/visitstutorial-cc3f0c43.svg)

#### Actions

Actions are located under the _packages_ directory and determined by the subdirectory structure. In this case, the subdirectory called _visits_ serves as a qualifier for the project's two actions. The _visits_ directory contains two PHP files, which are determined to be two actions: `visits/counter` and `visits/info`.

- The code for the `counter` action in _counter.php_ creates an instance of a [Redis key-value store](https://redis.io) that is built into the Nimbella Cloud. It checks for a cookie first, and if none is found, it increments the count by one and writes to the cookie.

- The `info` action checks for a file in the data bucket returns its contents, which are the date since the project was deployed. If it can't find the file, it creates one and adds the current date.

#### Static web content

The _web_ directory contains  static web content for the project. In this case, there is one HTML file and a logo image.

The _index.html_ file contains JavaScript that displays the number of unique visitors and the date that the count started.

### No other configuration or build instructions required

With this directory structure, you don't need any project  configuration or specific build instructions to deploy this project in the Nimbella Cloud. Just run the deployment command in the next section.


### Deploy this project to the Nimbella Cloud

If you have the [Nimbella command line tool called `nim`](https://nimbella.io/downloads/nim/nim.html#install-the-nimbella-command-line-tool-nim) installed, you can deploy this project directly from GitHub, either online or from the local repository  cloned to your  disk.

- Run the following command in your terminal:

   `nim project deploy /path/to/visits`

The output of this command will include a link to where the application is running in the cloud.
