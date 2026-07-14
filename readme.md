Slack Setup
* Create an app in Slack
* Enable Socket Mode to WebSocket. This enables the communication to happen over WebSocket instead of over HTTP
* Set up authentication token and app token in Slack app
* Set up authentication scope that creates permission on what the bot can do and cannot do. The bot can send messages, use slash commands, read mentions, and access channel messages.
* Install the app in the Hack Club Slack Workspace
* Set up the slash commands in Slack App

Coding
* Download and setup VS Code
* Create directories in local workstation where code will be built
* Create a folder where code will be built and change directory to this location
* Use node package manager (npm) to init and install slack/bolt and dotenv packages.
* Create a .env file and store the slack OAuth token and App-Level Token in the file.
* Create a .gitignore file to add node_modules and .env so that they are not committed into GitHub repository which is public.  
* Create index.js file 