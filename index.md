## Learn how to make a bot
### See this page

### Step 1: Creating your bot
Firstly, before you even think about writing any code, you will need to create your bot. You can do this by going to the [discord.com/developers/applications](discord dev portal) and creating a new application. Give it a catchy name, and then and an icon if you so desire. Next, go into the bot tab and click on create bot. Next, go into the Oauth tab and select the bot scope. Underneath this, there should now be a box for permissions. Choose your bot's required permissions then copy the link above. Paste this into a web browser and follow the steps to connect your bot to your server.

### Step 2: Package.json
Secondly, you're going to need a text editor, Visual Studio Code is reccomened but notepad works just as well. You will also need your computer's command prompt and an up-to-date version of [nodejs.org](Node.js and NPM). Open your command prompt by opening the run tab, WIN + R, and running "cmd" in the box. Navigate into the folder you would like to make you bot in by using the "cd 'your-folder-here'" command and to make a folder, just use the "mkdir 'your-folder-here'" command. Inside your folder, type "npm init" to create a package.json file. Fill in the questions NPM asks you, and make sure that the question called "main" is set to main.js. Next, you will need to install your packages, such as Discord.js. To install it, just run ```npm install discord.js --save```. That will add discord.js to your package.json file and you will be able to use it in main.js.

### Step 3: main.js
Thirdly, you will need to setup your main main.js file. Open up your text editor and create the ```main.js``` file. Let's take you through the code we will use.

```const Discord = require('discord.js');```
```const client = new Discord.Client();```
These consist Discord into the JavaScript file, and creates a client for the bot along with it.

```client.once('ready', () => {```
  ```console.log('Bot online!');```
```}```
This will tell us that the bot is online when it conencts to the API.

```client.on('message', message => {```
  ```console.log(message.content);```
```}```
This will tell us which messages are being send

```if (message.content === '!ping') {```
	```message.channel.send('Pong.');```
```}```
This will look for the !pong command being sent, and then will message "Pong.".

```client.login('your-token-goes-here');```
This will get your bot token, smash it on the API, and make your bot appear to anyone who sees it when you are running the code.

#### The code all at once
const Discord = require('discord.js');
const client = new Discord.Client();

client.once('ready', () => {
	console.log('Ready!');
});

client.on('message', message => {
	console.log(message.content);
	if (message.content === '!ping') {
    message.channel.send('Pong.');
    
  }
  
});

client.login('your-token-goes-here');

### Step 4: Running your bot
Now is the moment of truth, time to run your bot. Type ```node main.js``` into the cmd prompt, and then wait for it to say "bot online". Then go to the server you installed the bot into before and type in ```!ping```. You should get a response saying ```Ping.```. 

## What next?
Now, take a look at the [discordjs.guide](Discord.js documentation) to find out more stuff you can do, including embeds and custom arguments. Or take a look at our other guides and learn something else.

**Remember, there's something for everyone.**
