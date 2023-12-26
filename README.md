# Google API examples

## Contents

1. JS Client (GA4 Data API v1beta)
   - go to [https://max-ostapenko.github.io/api_examples/examples/ga4_client_js/data_api.html](https://max-ostapenko.github.io/api_examples/examples/ga4_client_js/data_api.html)
   - insert your CLIENT_ID
   - press `Authorize` button

2. Python server (Management API v1)
   - insert 'client_secret.json' file into the example folder
   - run:

        ```bash
        python server.py
        ```

## FAQ

1. How to get CLIENT_ID and CLIENT_SECRET?
   - go to https://console.developers.google.com/apis/credentials

2. How to get client_secret.json?
   - go to https://console.developers.google.com/apis/credentials

3. How to resolve authentication error 'unknown origin'?
   - add your domain to the list of authorized domains in the Google API Console. Your client_secret.json should look like this:

        ```json
        {
            "web": {
                "client_id": ...,
                "project_id": "max-ostapenko",
                "auth_uri": "https://accounts.google.com/o/oauth2/auth",
                "token_uri": "https://oauth2.googleapis.com/token",
                "auth_provider_x509_cert_url": "https://www.googleapis.com/oauth2/v1/certs",
                "client_secret": ...,
                "redirect_uris": [
                "https://max-ostapenko.github.io/api_examples/examples/ga4_client_js/data_api.html",
                "https://localhost/oauth2callback"
                ],
                "javascript_origins": [
                "https://max-ostapenko.github.io",
                "https://localhost"
                ]
            }
        }
        ```
