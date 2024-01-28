![image](https://github.com/AnanduVijay/Django--Google_Sign-in/assets/79689148/a0de8fb8-e80c-4021-aeb5-31946678a925)

# Django--Google_Sign-in
Google sign-in for django app
## Django app Setup
1.Create our Google sign in consent screen.And create a project 
   -  open Google [ API console](https://console.developers.google.com/apis)
   -  Create a APIs project
   -  Select your project
   - ![image](https://github.com/AnanduVijay/Django--Google_Sign-in/assets/79689148/149434cd-5988-4313-92dc-faf6082562e0)

2. Configure the OAuth consent screen.
     - Click Credentials > Create credentials > OAuth client ID.
     - Click Configure the consent screen > External > Create. Complete the form (I added example.com as the Authorized domain).
     - Add scopes to determine what information you want to access (I added email) > Save and Continue.
     - Add test Google account users (I added my email) > Save and Continue.
   - Click Back to Dashboard
3.  Create an OAuth client ID
    - Click Credentials > Create credentials > OAuth client ID > Web application.
    - Add authorized Javascript origins For our local development,
      add both http://localhost and http://localhost:8000 to Authorized JavaScript origins.
    - Add  Authorized redirect URIs
      ```bash
       http://localhost:8000/auth-receiver
      ````
    - Create and copy
    - Click create and copy the Client ID and Client Secret.
4. Add the Client ID to  Django app
   - Create a file called .env at config/.env and add the below to it.
     ```bash
     GOOGLE_OAUTH_CLIENT_ID=<your_client_id>
     ```
5. Also add this client id  in sign_in.html.
   ```bash
    data-client_id = "your_client_id"
   ```
  - ![image](https://github.com/AnanduVijay/Django--Google_Sign-in/assets/79689148/409ed4f4-34cc-480a-a7a3-cec8de7f2ed5)

## Installation

1. Clone repo
```bash
  git clone https://github.com/AnanduVijay/Django--Google_Sign-in.git
```
2. Use the package manager [pip](https://pip.pypa.io/en/stable/) to install requirements.txt

```bash
pip install -r requirements.txt
```

3. Run Migrations
```bash
py manage.py migrate
```
4. Run the Development Server

```bash
python manage.py runserver
```
