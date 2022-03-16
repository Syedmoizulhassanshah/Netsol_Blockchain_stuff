# Setting up environment for blockchain development  

**Note:** The instructions given below are for Ubuntu 20.04 LTS (users only).



## 1. Install Node.js

Node.js v16.13.2 or later

1. First, we will install the PPA in order to get access to its packages. From your home directory, use `curl` to retrieve the installation script for your preferred version, making sure to replace `16.x` with your preferred version string (if different),recommend is Node.js v16.13.2 or later.

```
- cd ~
-sudo apt install curl
-curl -sL https://deb.nodesource.com/setup_16.x -o /tmp/nodesource_setup.sh

```

Refer to the [NodeSource documentation](https://github.com/nodesource/distributions/blob/master/README.md) for more information on the available versions.

2. Inspect the contents of the downloaded script with `nano` (or your preferred text editor):

`nano /tmp/nodesource_setup.sh`

3. When you are satisfied that the script is safe to run, exit your editor, then run the script with `sudo`:

`sudo bash /tmp/nodesource_setup.sh`

 The PPA will be added to your configuration and your local package cache will be updated automatically.
 
5. You can now install the Node.js package:

`sudo apt install nodejs`

6. Verify that you’ve installed the new version by running `node` with the `-v` version flag:

`node -v`

 **Output**:`v16.6.1`

7. The NodeSource `nodejs` package contains both the `node` binary and `npm`, so you don’t need to install `npm` separately.

At this point you have successfully installed Node.js and `npm` using `apt` and the NodeSource PPA.
You can install node.js with many other ways by following the guide present in this [link](https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-20-04).


## 2. Install Ganache
This guide will use the desktop version of Ganache. Ganache will provide a personal blockchain to be used for local development and testing of smart contracts.
1. In Ubuntu, open a browser and navigate to [https://trufflesuite.com/ganache/index.html](https://trufflesuite.com/ganache/index.html)
2. Download the latest Linux release which will be the `*.AppImage file.`
For example `ganache-1.3.0-x86_64.AppImage.`
3. Once the download is complete, open a new terminal and change into the directory with the `*.AppImage file.`
4. Use chmod to make the file executable:
 `chmod a+x ganache-1.3.0-x86_64.AppImage`
5. Now run the file
`./ganache-1.3.0-x86_64.AppImage`
6. You will be prompted if you want to integrate the application into your system. For convenience, click **Yes**. This will allow you to launch Ganache later from Ubuntu Application menu.
7. you can also install Ganache's CLI version by running `sudo npm install -g ganache-cli` command in the terminal, for more details refer to the **Ganachi CLI** section in this [link](https://medium.com/compound-finance/setting-up-an-ethereum-development-environment-7c387664c5fe) or can follow the steps present in [Ganache's Github](https://github.com/trufflesuite/ganache).
8. To see whether Ganache's CLI version is installed properly or not run `ganache-cli` command in the terminal, if you see an output like this , you are good to go, its  installed!

![Ganache-cli](https://user-images.githubusercontent.com/52605353/158597938-9d8a4823-47e2-489f-b218-caef0c0573be.png)

 

## 3. Install Blockchain Development Framework

- Before installing the Truffle Framework  make sure that your `npm` version is 8.5.4 or above, by running this command `npm -v` in the terminal.

- If the `npm` version is not 8.5.4 or above , then run `sudo npm install -g npm@8.5.4` before running the truffle installation command, in order to avoid the error shown in the sample image below.

![npm issue](https://user-images.githubusercontent.com/52605353/158598408-797e3435-d64e-4517-93fa-b343d6961ff1.png)


### **a) Truffle (Recommended)**
You can install truffle using this command:
`sudo npm install -g truffle`

For more details see [Truffle Docs](https://trufflesuite.com/docs/truffle/getting-started/installation.html).

### **b)  Hardhat (alternative framework)**

You can follow the [Hardhat Docs](https://hardhat.org/tutorial/creating-a-new-hardhat-project.html) to setup the hardhat,if the project is to be build using Hardhat. 

## 4. Install Metamask extension on chrome or firefox. (To connect with web3)

1. Go to [Metamask Website](https://metamask.io/download/)
2. Click **Get Chrome Extension** to install Metamask.
3. Click **Add to Chrome** in the upper right
4. Click **Add Extension** to complete the installation.
5. You will know Metamask has been installed when you see the fox logo on the upper right hand corner of your browser.

 
## 5. Install VS-Code
To install the VS Code snap 
1. open your terminal (Ctrl+Alt+T) 
2. Run the following command: `sudo snap install --classic code`. That’s it. Visual Studio Code has been installed on your Ubuntu machine.
3. If you prefer using a GUI, open Ubuntu Software, search for “Visual Studio Code” and install the application:

![VS-Code](https://user-images.githubusercontent.com/52605353/158600243-cd80a5c5-550e-4838-9667-6e576e126a3e.png)

4.For Installing Visual Studio Code with `apt` you can follow **Installing Visual Studio Code with apt** section present in this [Guide](https://linuxize.com/post/how-to-install-visual-studio-code-on-ubuntu-20-04/) . 
 

## 6. Install Web3.js

- You can install Web3.js library by running `npm install web3` command in the terminal when you are in your project directory.
- For more details refer to the **Installing Web3.js** section in this [link](https://medium.com/compound-finance/setting-up-an-ethereum-development-environment-7c387664c5fe)

## 7. Install MongoDB

You can install MongoDB by following this [Guide](https://www.digitalocean.com/community/tutorials/how-to-install-mongodb-on-ubuntu-20-04)


