# Python Gmail IMAP

Code based on own experience and some codes I couldn't find the sources, sorry. **Python Gmail IMAP** was written to help community with code that isn't clearly documented. You can find a step by step on how to get the credentials you'll need to run the code.

It's not meant to be an IMAP client, instead, just a piece of code to built in your projects.

## Usage
Firstly, clone the repository and access it's directory:
```
git clone https://github.com/rcbonz/Python-Gmail-IMAP.git
```
```
cd Python-Gmail-IMAP
```
```
python3 pythonGmailImap.py
```

## Getting it to work
Follow the steps to get the required credentials on Google Console [here](#creating-google-credentials) and with your **Client ID** and **Client Secret**, run the following command on terminal:
```
python2 oauth2.py --generate_oauth2_token --client_id=<your client id> --client_secret=<your client secret>
```
> The original oauth2.py file can be found [here](https://github.com/google/gmail-oauth2-tools/tree/master/python).

This command will generate a link to allow the IMAP to be used on you e-mail account, as follows:
![](https://github.com/rcbonz/Python-Gmail-IMAP/blob/main/gmail_imap_005.png?raw=true)

Access the link in a browser and follow the steps till you get the Authorization Code and copy it. Go back to the terminal and paste it:
![](https://github.com/rcbonz/Python-Gmail-IMAP/blob/main/gmail_imap_006.png?raw=true)

Now you have the refresh token that you'll need to run the IMAP client.
![](https://github.com/rcbonz/Python-Gmail-IMAP/blob/main/gmail_imap_007.png?raw=true)

Paste all credentials in the `pythonGmailImap.py` and run it:
```
python3 pythonGmailImap.py
```
## Creating Google Credentials
Access the [Google Console](https://console.cloud.google.com/) page and follow the steps:

1. Create a new project and search for the **Gmail API** on the API Library tab, then open it and **Enable** it.

![](https://github.com/rcbonz/Python-Gmail-IMAP/blob/main/gmail_imap_001.png?raw=true)

2. In the **Gmail API** details tab, click on **Credentials** and than in **Create Credentials**. Choose the **OAuth client ID**

![](https://github.com/rcbonz/Python-Gmail-IMAP/blob/main/gmail_imap_002.png?raw=true)

3. Select **Desktop app** as the application type and finish creating it.

![](https://github.com/rcbonz/Python-Gmail-IMAP/blob/main/gmail_imap_003.png?raw=true)

4. There are your **Client ID** and **Client Secret**.

![](https://github.com/rcbonz/Python-Gmail-IMAP/blob/main/gmail_imap_004.png?raw=true)

