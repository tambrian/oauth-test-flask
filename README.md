# OAuth 2.0 Test (using Flask)

A simple OAuth 2.0 implementation with Google.

## Table of contents
* [Setting up OAuth 2.0 on Google's website](#setting-up-OAuth-2.0-on-Google's-website)
* [Installation](#installation)
* [Running Locally](#running-locally)

## Setting up OAuth 2.0 on Google's website

Google Sign-In manages the OAuth 2.0 flow and token lifecycle, simplifying your integration with Google APIs.

* Before you can integrate Google Sign-In into your website, you must create a client ID, which you need to call the sign-in API.
* To create a Google API Console project and client ID, [head to the Google Developers Console](https://console.developers.google.com/).
  * If you do not have any projects, you should see a "Create Project" link on the right-hand side of the page.
  * Otherwise, you could choose existing projects (or create another project by clicking on the downward arrow on the upper left hand side - next to the Google APIs logo).
* Then, fill in the required information and select "Next".
* On the left-hand side, select "OAuth consent screen" and fill in the requested information.
* Again on the left-hand side, select "Credentials" and then "Create Credentials (OAuth client ID)" to access the API.
  * Choose "Web Application" for Application Type.
  * For "Authorized JavaScript origins" and "Authorized redirect URIs":
    * Put [http://localhost:5000](http://localhost:5000) (Port 5000 is default for Flask).
* Lastly, you will be given the "Client ID" (remember not to push any code with the Client ID up to GitHub).
  * Place this in the [home.html](./templates/home.html) file under the content attribute of the meta element.


## Installation

Clone Repo
```sh
git clone https://github.com/tambrian/oauth-test-flask.git` # or clone your own fork
```

## Running Locally

```sh
FLASK_APP=api.py flask run
```

Your app should now be running on [localhost:5000](http://localhost:5000).
