# Security analysis framework setup for solidity smart-contracts with detail

Here, the security analysis frameworks that we recommend for smart-contracts are **Mythril** and **Slither** , for a detailed comparison you can see the **Finalized Security Frameworks list for Smart-contracts Analysis (POC) v0.1.ods file** present above.

**Note:** The instructions given below are for Ubuntu 20.04 LTS (users only).

## Mythril

### Tool Description

- Mythril is a tool which allows the symbolic execution of the EVM bytecode and generates a flow control graph.
- It performs static analysis and formal verification of the smart-contract and does not support dynamic analysis. Refer this [link](https://www.sciencedirect.com/science/article/pii/S0140366421001043) for more details.
- Developed by the company ConsenSys, is available on Github  from September 2017. 
- It can perform in two ways, analysing .sol extension files  and giving, as a parameter, the contract address from the Ethereum blockchain. 
- For more details you can check this [link]( https://github.com/ConsenSys/mythril)

### Installation Process

To setup Mythril for your project:

1. On your work-machine you need to have following dependencies installed : `npm, python3,pip3` 
2. Now go to your project directory and open the terminal OR open the project directory in VS-CODE.
3. Run the following command in the termninal `pip3 install mythril`, this will install mythril into your project directory with the help of `pip3`.
4. Or In order to install Mythril using Docker, run the following command in the terminal  `docker pull mythril/myth`, for this you need to have docker installed on your work-machine already.
5. For more details you can check the **Installation and setup** section in this [link](https://github.com/ConsenSys/mythril).

### Analyzing the Smart-contract

To analyze the smart-contract

1. Navigate to the folder or directory where your smart-contracts are residing.
2. Run the following command in the terminal `myth analyze <solidity-file>` and wait for the results.
3. For more details you can check  the Usage section in this [link](https://github.com/ConsenSys/mythril)

### Sample contracts Tested

Following are the sample smart-contracts that we tested:

  a) [Re-entrancy]( https://github.com/sigp/solidity-security-blog#1-re-entrancy-1)
  b) [over-flow/under-flow](https://github.com/sigp/solidity-security-blog#1-re-entrancy-1) 
  c) [Ethereum Bank](https://github.com/Syedmoizulhassanshah/Solidity_For_Newbies/blob/main/My%20Ethereum%20Bank.txt)

for more detailed analysis and sample test smart-contracts kindly see the [link](https://github.com/sigp/solidity-security-blog#1-re-entrancy-1)

### Add Custom Analysis Modules

We can add custom analysis modules in [analysis/module/modules](https://github.com/ConsenSys/mythril/tree/develop/mythril/analysis/module/modules) and they are to be written in python.

### Remarks

- It shows results and also defines the severity of the vulnerability.
-  Results are shown in around 30s – 60s for small contracts and can take more than 60s for large contracts. 
- It also shows the vulnerabilities along with line number  on which it is present.
- Results are detailed.
- It also tells the estimated gas usage.
- It gives the initial state of the contract along with the sequence in which the transaction have been executed. 

### Results

  - when you will clone the **Security framework setup** repository.
  - And follow the above guide for analysing the smart-contracts using Mythril,you will see the following outputs in your terminal 
  - This shows that you have followed the guide properly.

[Re-entrancy]( https://github.com/sigp/solidity-security-blog#1-re-entrancy-1)

![Mythril Reentrancy](https://user-images.githubusercontent.com/52605353/158335161-2820a903-f3db-47d7-a7d7-ab11c47cf79f.png)

[over-flow/under-flow](https://github.com/sigp/solidity-security-blog#1-re-entrancy-1) 

![Mythril Over_or_Under_Flow](https://user-images.githubusercontent.com/52605353/158335215-35393b0a-c698-4ab8-b472-36a69ad8f271.png)



## Slither

### Tool Description
- Slither is a static analysis framework written in Python 3 with dependencies on the Solidity Compiler (Solc). 
- It performs static analysis only does not support dynamic analysis and formal verification. Refer this [link](https://www.sciencedirect.com/science/article/pii/S0140366421001043) for more details.
- It is available on Github from September 2018 (AGPL-3.0 license).
- Average execution time of less than 1 second per contract.
- For more details you can check this [link](https://github.com/crytic/slither)

### Installation Process

To setup slither for your project:

1. On your work-machine you need to have following dependencies installed : `solc, python3` 
2. Now go to your project directory and open the terminal OR open the project directory in VS-CODE.
3. Run the following command in the termninal `pip3 install slither-analyzer`, this will install slither into your project directory with the help of `pip3`.
4. Or In order to install slither using Docker, run the following command in the terminal  `docker pull trailofbits/eth-security-toolbox`, for this you need to have docker installed on your work-machine already.
5. For more details you can check the **How to install** section in this [link](https://github.com/crytic/slither).

### Analyzing the Smart-contract

To analyze the smart-contract

1. Navigate to the folder or directory where your smart-contracts are residing.
2. Run the following command in the terminal `slither <folder name>/<solidity-file>` and wait for the results.
3. For more details you can check the **Bugs and Optimizations Detection** section in this [link](https://github.com/crytic/slither).

### Sample contracts Tested

Following are the sample smart-contracts that we tested:

  a) [Re-entrancy]( https://github.com/sigp/solidity-security-blog#1-re-entrancy-1)
  b) [over-flow/under-flow](https://github.com/sigp/solidity-security-blog#1-re-entrancy-1) 
  c) [Ethereum Bank](https://github.com/Syedmoizulhassanshah/Solidity_For_Newbies/blob/main/My%20Ethereum%20Bank.txt)

for more detailed analysis and sample test smart-contracts kindly see the [link](https://github.com/sigp/solidity-security-blog#1-re-entrancy-1)

### Add Custom Analysis Modules

We can add custom analysis modules in [slither/analyses/](https://github.com/crytic/slither/tree/master/slither/analyses) and they are to be written in python.

For details kindly see this [link](https://blog.trailofbits.com/2018/10/19/slither-a-solidity-static-analysis-framework/)

### Remarks

  - It shows results , but does not define the severity of the vulnerability.
  - Results are shown in few seconds.
  - It shows the vulnerabilities along with line number on which they is present.
  - Results are not that detailed.

### Results
   
  - when you will clone the **Security framework setup** repository.
  - And follow the above guide for analysing the smart-contracts using slither,you will see the following outputs in your terminal 
  - This shows that you have followed the guide properly.
  
 [Re-entrancy]( https://github.com/sigp/solidity-security-blog#1-re-entrancy-1)
 
![Slither Reentrancy](https://user-images.githubusercontent.com/52605353/158323061-50147096-b652-49b8-9a57-12cc1130e115.png)



   [over-flow/under-flow](https://github.com/sigp/solidity-security-blog#1-re-entrancy-1) 
  
  
![Slither Over_or_UnderFlow](https://user-images.githubusercontent.com/52605353/158323105-9781e6f7-a495-494c-a82f-39a047e24617.png)


## Useful References

For more detail kindly refer to the links given below:

1. [A security framework for Ethereum smart contracts (Reseach Work)](https://www.sciencedirect.com/science/article/pii/S0140366421001043)
2. [Mythril’s documentation](https://mythril-classic.readthedocs.io/en/develop/)
3. [An Analysis of Smart Contracts Security Threats Alongside Existing Solutions](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7516633/)
4. [Ethereum Doc for smart-contracts security](https://ethereum.org/en/developers/docs/smart-contracts/security/)


