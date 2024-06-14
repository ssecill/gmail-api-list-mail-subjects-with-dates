# Gmail API Usage Guide

This guide demonstrates how to list email subjects within a specified date range using the Gmail API in Python.

## Requirements

1. Python 3.x
2. Required Python libraries:
   - google-api-python-client
   - google-auth-httplib2
   - google-auth-oauthlib
3. A project in Google Cloud Console and OAuth 2.0 client credentials (`credentials.json` file).

## Steps

### 1. Install Required Libraries

Use the following command to install the required libraries:

```sh
pip install --upgrade google-api-python-client google-auth-httplib2 google-auth-oauthlib pandas openpyxl
```

### 2. Create a Project in Google Cloud Console and Enable Gmail API

1. Go to [Google Cloud Console](https://console.cloud.google.com/) and select your project or create a new one.
2. In the left menu, go to "APIs & Services" and click on "Library".
3. In the search bar, type "Gmail API" and click on the result.
4. Click the "Enable" button.

### 3. Create OAuth 2.0 Client Credentials

1. In the left menu, go to "APIs & Services" and click on "Credentials".
2. Click on the "Create Credentials" button and select "OAuth client ID".
3. Select "Desktop app" as the "Application type" and enter a name.
4. Click the "Create" button and download the client ID and secret.
5. Save the `credentials.json` file in the same directory as your Python script.

### 4. Run the Python Code

Run the Python script:

```sh
python gmail_api.py
```

When the code is run for the first time, an OAuth 2.0 authorization page will open in your browser, asking you to sign in with your Google account. Once authorization is complete, the script will list email subjects within the specified date range.

## Notes

- Ensure that the `credentials.json` file contains the client credentials downloaded from Google Cloud Console.
- The first time the script is run, an authorization window will open to request user consent. Once consent is given, a `token.json` file will be created, eliminating the need for reauthorization in the future.
- The date format should be `YYYY/MM/DD`. Adjust the date range in the code to suit your needs.

This guide will help you use the Gmail API to list email subjects within a specified date range. If you have any questions, feel free to ask!
