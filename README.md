# AndroCI

A beautiful Travis CI client!

## Libraries in Use
- [**Retrofit**](https://github.com/square/retrofit) for constructing the REST API
- [**Picasso**](https://github.com/square/picasso) for loading images
- [**Gson**](https://github.com/google/gson) to convert Java objects to JSON and vice-versa
- [**Gson Converter**](https://github.com/square/retrofit/tree/master/retrofit-converters/gson) for serialization to and from JSON


_AndroCI is under active development. More features are on their way!_

## Usage

### Setup

#### Prerequisites
- To work on this repo on your local environment, you would need to generate register your flavour of this app with GitHub in order to access the GitHub OAuth API.
  - Please follow the steps [here](https://developer.github.com/apps/building-oauth-apps/creating-an-oauth-app/), in order to set up your credentials for using this app.

#### Setting up the project in Android Studio
- Once you are done with this, create a file with the name "dubug_gradle.properties", and paste the following code:
```groovy
github_client_id=<Client ID Generated in Step 1>
github_secret=<Secret ID Generated in Step 1>
redirect_url=androci://callback
```
- Change the `Build Variants` of both the main App and the APICommunicator Library to `debug`.
- Now, just rebuild the project in android studio, and it should work.

### Package Structure
The app is divided into two Components:
- The `APICommunicator` Library, which provides an interface to make API Calls and Authorization Requests via GitHub and Travis APIs.
- The `AndroCI` app, which is basically a front end, and has the `APICommunicator` Library as a dependency.

