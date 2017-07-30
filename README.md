# Lending Platform Prototype - Basic version using Ethereum. Still needs a lot of work.

Money Lending Platform  

My objective is to build a decentralized money lending platform. 
Implementation: A decentralized money lending platform with deadline and asset storage and verification proponents. 
 

What I can support right now: Lending, Borrowing, Paying debts currently but it does not support a deadline functionalty. 
I have also built a basic asset declaration smart contract which maps a document hash (Assuming every property has a document, whose hash is uploaded to the Blockchain for verification purposes.
The contract simulates a company taking money from the lenders and lending it to borrowers and thus earning commission in the process.

I need to improve the asset storage and verification process; I'm planning to add a deadline facility in near future which will help the contract owner as well as borrower the facility of alarm which will inform him about paying debts.

Quick guide: Instructions to run the code

Basic requirements: 

i) testrpc 
ii) npm,node-js, web3js 
iii) truffle 

Steps to follow:

         1) Start "testrpc" in one terminal by typing just 'testrpc'.

         2) Open another terminal and go into project directory then run the following commands one by one: i) run the command:  > truffle compile      (this will compile the contract codes in /contract directory)
        ii)run the command:  > truffle migrate      (it will deploy the contract locally)
        iii)runt the command: > System.deployed()   (Copy the contract address from o/p and initialize each 'contract_address' variable in all js files(i.e first line variables of : public/javascripts/lenderjs.js and public/javascripts/borrowerjs.js).
        iv)run the command: > Asset.deployed()       (copy the contract address from o/p and each 'contract_address' variable in asset.js and verify.js files stored in 'public/javascripts/' directory.

       3) Now start another terminal and go to the project directory and run the project using nodejs using the command:  > node server.js         (this file will start project on localhost:8000).

       4) Now can be accessed using:
          i)localhost:8000/lender    (this will open lender services such lend,withdraw, register etc)
          ii)localhost:8000/borrower  (this will open borrower services such as borrow,pay_debts,register etc)
         iii)localhost:8000/asset     (this will open the asset registration form)
         iv)localhost:8000/verify     (this will open the page to verify the ownership of asset)
