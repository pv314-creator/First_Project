**Description**
* This project is a Slack bot built using node.js, the Slack bot framework, and Axios. The bot responds to slash commands in Slack and can check its latency, provide random cat facts, display random rokes, and list all avaliable commands.

**How the bot was made**
1. Created a Slack app and enabled Socket Mode for WebSocket communication.
2. Generated the Slack Bot Token and App Token.
3. Configured the bot's OAuth scopes to allow it to:
   - Respond to slash commands
   - Send messages
4. Installed the app into the Slack workspace.
5. Created the project using **Node.js** and installed the required packages:
   - `@slack/bolt`
   - `axios`
   - `dotenv`
6. Stored the Slack tokens in a `.env` file and added both `.env` and `node_modules` to `.gitignore`.
7. Wrote the bot logic in `index.js`:
   - Initialized the Slack Bolt app.
   - Loaded the authentication tokens from the environment variables.
   - Created asynchronous handlers for each slash command.
   - Used Axios to retrieve data from external APIs for the cat fact and joke commands.
8. Started the bot with:

```bash
node index.js
```
Once running, the bot listens for slash commands and responds directly in Slack.

**Command**

### `/pv-help`

Displays a list of all available commands.

### `/pv-ping`

Measures the bot's response latency and confirms that it is online.

**Example Output**

```
Yo yo ma!!!
Latency: 15ms
```

---

### `/pv-catfact`

Retrieves a random cat fact using the Cat Fact API.

**API Used**

- https://catfact.ninja/fact

**Example Output**

```
Cat Fact:
Cats can rotate their ears 180 degrees.
```

---

### `/pv-joke`

Retrieves a random joke using the Official Joke API.

**API Used**

- https://official-joke-api.appspot.com/random_joke

**Example Output**

```
Why don't scientists trust atoms?
Because they make up everything.
```
