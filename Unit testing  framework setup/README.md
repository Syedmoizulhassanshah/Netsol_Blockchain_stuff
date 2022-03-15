# Unit Testing framework setup for smart-contracts testing

Here, the Unit testing framework that we recommend for smart-contracts is **Truffle Test**,although if you are using Hardhat framework then **Waffle** is the test tool that is recommended.For a detailed comparison you can see the **Final_UnitTesting_v0.2.xls** file present above.

**Note:** The instructions given below are for Ubuntu 20.04 LTS (users only).

## Truffle Test

### Tool Description

Truffle is a world class development environment, testing framework and asset pipeline for blockchains using the Ethereum Virtual Machine (EVM), aiming to make life as a developer easier. With Truffle, you get:

- Built-in smart contract compilation, linking, deployment and binary management.
- Automated contract testing for rapid development.
- Scriptable, extensible deployment & migrations framework.
- Network management for deploying to any number of public & private networks.
- Package management with EthPM & NPM, using the ERC190 standard.
- Interactive console for direct contract communication.
- Configurable build pipeline with support for tight integration.
- External script runner that executes scripts within a Truffle environment.

### Installation Process

To install Truffle for your project:

1. On your work-machine you need to have following dependencies installed : `NodeJS v12 or later`, 
`Windows, Linux or Mac OS X`.
2. Now open your terminal and run the following command `npm install -g truffle`, this will install truffle globally on your machine.
3. Now go to your project directory and open the terminal OR open the project directory in VS-CODE.
4. Run the following command in the termninal `truffle init`, this will initialize a truffle project.
5. After the truffle project is initialized you will have three new folder named as **contracts**, **migrations** and **test** in your project directory along with a **truffle- config.js** file.
6. We will always place our tests in the **test** folder. 

### Testing the contracts

In order to execute the Truffle-test:

1. Go to your project directory and open the terminal OR open the project directory in VS-CODE.
2. Setup `ganache` and deploy contract.
3. Create `.js` file in the test folder and write test in it.
4. Import contract artifacts in the `.js` file you created.
5. Now navigate to the test folder and run `truffle test` command in the terminal to run all the test or alternatively, you can specify a path to a specific file you want to run, e.g., `truffle test ./path/to/test/file.js`.
6. When the truffle test process exits, its exit code is equal to the number of failing tests. If there are more than 255 failing tests, it will exit with code 255.
7. For more details see the **Testing** portion in the [Truffle Docs](https://trufflesuite.com/docs/truffle/testing/testing-your-contracts.html)

### Remarks
In a blockchain environment, a single mistake could cost you all of your funds - or even worse, your users' funds! This guide will help you develop robust applications by writing automated tests that verify your application behaves exactly as you intended.

1. Truffle comes standard with an automated testing framework to make testing your contracts a breeze.
2. This framework lets you write simple and manageable tests in two different ways:
   - In **Javascript** and **TypeScript**, for exercising your contracts from the outside world, just like your application.
   - In **Solidity**, for exercising your contracts in advanced, bare-to-the-metal scenarios.
    Both styles of tests have their advantages and drawbacks.
3. All test files should be located in the `./test` directory. Truffle will only run test files with the following file extensions: `.js`, `.ts`, `.es`, `.es6`, and `.jsx`, and `.sol`. All other files are ignored. 
4. Truffle smart-contract test framework is mostly **recommended**.


### Results
- when you will clone the **Unit Testing framework setup** repository. 
- And run the tests properly you will see an output like this in your terminal.
- This shows that you have followed the guide properly. 

![Unit test results](https://user-images.githubusercontent.com/52605353/158319190-dd39fa7b-2930-4fa7-9556-096796e3a580.png)




## Waffle (alternative ,used for Hardhat)
- It works with hardhat framework just like Truffle.
- Comparitively faster than Truffle, Fast compilation.
- For installing waffle with Npm we run `npm i ethereum-waffle` command in the terminal of our project directory.For more details see **How to install** section [here](https://getwaffle.io/) or refer to [Waffle Github](https://github.com/TrueFiEng/Waffle)
- For more details regarding Waffle tool see [Waffle Github](https://github.com/TrueFiEng/Waffle)

## Useful References 
1. [Truffle Docs](https://trufflesuite.com/docs/truffle/testing/testing-your-contracts.html)
2. [Hardhat Docs](https://hardhat.org/tutorial/testing-contracts.html)
3. [Waffle Docs](https://ethereum-waffle.readthedocs.io/en/latest/)
4. [Waffle Github](https://github.com/TrueFiEng/Waffle)

