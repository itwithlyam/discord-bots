## Learn how to make a bot
### See this page

### Step 1: Creating your bot
Firstly, before you even think about writing any code, you will need to create your bot. You can do this by going to the (discord dev portal)[discord.com/developers/applications] and creating a new application. Give it a catchy name, and then and an icon if you so desire. Next, go into the bot tab and click on create bot. Next, go into the Oauth tab and select the bot scope. Underneath this, there should now be a box for permissions. Choose your bot's required permissions then copy the link above. Paste this into a web browser and follow the steps to connect your bot to your server.

### Step 2: Package.json
Secondly, you're going to need a text editor, Visual Studio Code is reccomened but notepad works just as well. You will also need your computer's command prompt and an up-to-date version of (Node.js and NPM)[nodejs.org]. Open your command prompt by opening the run tab, WIN + R, and running "cmd" in the box. Navigate into the folder you would like to make you bot in by using the "cd 'your-folder-here'" command and to make a folder, just use the "mkdir 'your-folder-here'" command. Inside your folder, type "npm init" to create a package.json file. Fill in the questions NPM asks you, and make sure that the question called "main" is set to main.js. Next, you will need to install your packages, such as Discord.js. To install it, just run ```npm install discord.js --save```. That will add discord.js to your package.json file and you will be able to use it in main.js.
