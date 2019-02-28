# Auth0 Rules and Clients Python Web App Sample

## Sign in to your Auth0 management account 

## Navigate to Applications:
- Create Application
- Create a name for you application
- Choose Regular Web App
- Go to the Settings tab
    - Add the following to Allowed Callback URLs:
        http://localhost:3000/complete/auth0
    - Add the following to the Allowed Logout URLs:
        http://localhost:3000/
- Save

## Navigate to Rules:
- Create a Rule
- Pick "Whitelist for a Specific App"
- Replace "NameOfTheAppWithWhiteList" with the name of the application you just created
- Replace "'user1@example.com', 'user2@example.com'" with your whitelisted users, be sure to follow this format.
- Save

## Navigate to APIs:
- Select Auth0 Management API
- Select Machine To Machine Applications
- Authorize the app you just created

# Clone this repository to your machine
- Change the .env.example file to .env, add your client id, domain, and secret (these can be found in your application page on manage.auth0.com)

# In the command line of the machine you are running the application on:
Make sure Python is installed and execute the following commands in the sample's directory
    pip install -r requirements.txt
    python server.py

# On a browser on that machine
- Navigate to //localhost:3000
- Login with whitelisted user (non-whitelisted users with throw an error)
- You should see your clients and all of their rules

## Issue Reporting

If you have found a bug or if you have a feature request, please report them at this repository issues section.
Please do not report security vulnerabilities on the public GitHub issue tracker. 
The [Responsible Disclosure Program](https://auth0.com/whitehat) details the procedure for disclosing security issues.

## Author

[Auth0](https://auth0.com)

## License

This project is licensed under the MIT license. See the [LICENSE](LICENCE) file for more info.
