# Treasury Wallet

A tool for DAOs to manage the funds of the organization, fund projects, teams, and contributors, all through one simple interface that helps  
save on gas costs when transferring funds. 

---

## Why?
DAOs have money, and they're funding the coordination that goes into developing the protocols, platforms, and ideas that advance the crypto ecosystem.  

The most common practice is utilizing multisig wallets for each layer of the organization. Each team, each project, and every contributor, all need funding.  
The daily transfer of funds ends up costing a substantial amount in gas fees incurred each time the tokens are transferred, leaving less available for  
creating and developing. 

## Goal
This Treasury Management wallet will allow DAOs to allocate funds from a top down multisig contract, without necessitating external transfers for others to  
to obtain control over the funds.

## How?
Each external address, representing a team, a project, or a contributor, will register with the contract, being added to the whitelist. These can be multi-sig   wallets or individuals. When funding is approved, the Treasury Controller will allocate funds to the approved teams or projects by allocating funds as being  
available for those users to withdraw or spend. Those secondary accounts can also re-allocate funds to individuals as a form a payment for services rendered.  
The accounts cannot revoke access to the funds, but can only re-allocate them from the various approved pools. 

---

## Process
- The treasury will deploy the contract and become the owner.
- The owner will transfer the funds into the contract under the owner address.
- Other addresses will register to the contract by interacting with it. 
- The owner will approve specific addresses for the amount of funds specified by governance.
  - These accounts will be teams, groups, or individual projects.
  - Governance will be held externally from this contract currently.
  - Future revisions could allow voting within the contract to approve funding.
  - If voting is integrated, it should utilize an anti-sybil mechanism or if token based, quadratic voting, through a 'sign message' to save gas.
- The accounts with funds approved to them are able to withdraw from the contract to the external address, or re-allocate to other addresses.
- Any account with an approved balance allocation has sole control over those funds.
- The owner cannot reallocate funds from other addresses.
- In the event the contract halts or the GUI goes offline, funds should be recoverable by each address. 

---

## User Interface

The users will be able to interact with the smart contract from a website.  
The webiste will show token holdings and distributions made. This will allow for enhanced transparency of DAO governance and management.  
External vendors will be able to submit payments to the correct account through the website.  
Inflows, outflows, holdings, and allocations will be made visible as part of the dashboard.
