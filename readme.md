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
** In this file, require slack bolt library and axios library. 
** Read the OAuth and App-Level token into a constant
** Create a function that handles the Slack command. 
*** First function handles /dsb-ping. This command works asynchronously and takes 3 variables that Slack passes and responds back with a value for latency. 
*** Create a second function that handles /dsb-catfact. This command works asynchronously and takes 2 variables. Inside this function, using the axios library, make an HTTP call to catfact.ninja/fact. Wait till the site responds and grab the fact from the response data object. 
*** Create a third function that handles /dsb-joke. This command works asynchronously and takes 2 variables. Inside this function, using the axios library, make an HTTP call to official-joke-api.appspot.com/random_joke. Wait till the site responds and grab the setup and punchline from the response data object. 

Running
* From the command line, run node index.js. If deployed to any cloud environment, run the index.js as a service. 