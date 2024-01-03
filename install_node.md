- Install a Specific Node.js Version with NodeSource

```
sudo curl -sL https://deb.nodesource.com/setup_20.x -o nodesource_setup.sh
sudo bash nodesource_setup.sh
sudo apt install nodejs
node -v
```

- Install Node.js and NPM Using NVM

```
-- install nvm
sudo curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh
sudo curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"
nvm -v
nvm ls-remote

-- install node
nvm install `node-version`
```

- How to Remove Node.js from Ubuntu Server?

```
apt remove nodejs
apt purge nodejs
nvm current
nvm deactivate
nvm uninstall node_current_verion
```
