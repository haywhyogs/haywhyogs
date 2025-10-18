# SSH & Node.js Snippets

This file contains all the commands run so far while learning SSH, connecting to an Azure VM, setting up a Node.js application, running it, and debugging it. Each command includes a brief explanation.

```bash

# Install Node.js LTS
curl -sL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
sudo apt-get install nodejs -y

# First line adds Node.js LTS repository
# Second line installs Node.js
# -y automatically confirms installation prompts

# Install Express generator globally
sudo npm install -g express-generator
# -g = global installation, so you can create apps anywhere

# Create a new Express app with Pug template engine
express myExpressApp --view pug
# Creates a new app called myExpressApp
# --view pug sets Pug as the template engine

# Start the app
npm start
# Runs the Node.js Express app
# By default, the app listens on port 3000

# Forward port 3000 via VS Code Remote-SSH to access locally
# Lets you browse the remote web app at http://localhost:3000

# Debugging in VS Code
# Open the app via Remote-SSH in VS Code
# Click the gutter next to a line number (e.g., line 10) to set a breakpoint
# Run the debugger; execution stops at the breakpoint for inspection
# Allows full remote debugging without downloading source code locally