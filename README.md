# https://lottery-game-graph-chainlink-vrf.vercel.app/

## Requirements 
install `node` in your system

## Instruction on how to run this Project 
``` shell
cd interface
nom install
npm run dev
```
or
``` shell
cd interface
yarn
yarn dev
```

## Rules and Description
In this game, there are two type of parties e.g. the host and the player. Host is the deployer of smart contract. Only the host can host a game. The host has the power to determine entry fees (which a player have to pay to play the game) and number of maximum players to participate. The players have to pay the fees that the host determined to enter the game. After all the players joining, the smart contract will randomly choose a winner using ChainLink VRF among the player. The winner will get all the fees that the other players submitted at the beginning of the game (including winners fees too). The results will be shown with the game id and winner's wallet address. There are some important criteria of this DApp. 1. There will be always 1 game at a time. The host cannot host multiple game at a time. To host 2nd game , the 1st game have to be finished. 2. The game will not ended unless all the players are joined which was determined by the host at the beginning of the game and also pay the entry fees that was also determined at the beginning of the game. 3. Each player also have to pay 1 Link to play the game. 

## Inspiration
I was always wanted to build a game with blockchain but a proper game takes a lot of resources, time and knowledges. After learning ChainLink VRF, I thought this game might be the easiest implementation.

## What it does
This game basically picks a random Winner among a number of players. The host determines entry fees and max number of player. After the join of all the player with entry fees the game starts and picks a winner. The winner gets all the entry fees of other players including his.

## How we built it
The smart contract is built with Solidity, Hardhat, OpenZeppelin and deployed on Polygon network. Also ChainLink VRF is used for randomness. For node provider service Quick Node is been used. As for the the frontend Next.js framework and ether.js are been used and Web3Modal is used for set up the wallet. Also The Graph is been used for catching the events from smart-contract to show on front-end.

## Challenges we ran into
We all know blockchain is very deterministic in nature. So, randomness is a very big issue for Blockchain but thanks to ChainLink VRF function by which blockchain can communicate with outside data. Also implementing the graph is very big challenging too. It was very important to catching all the events from blockchain. So that it can be rendered on front-end.

## Accomplishments that we're proud of
We know traditional "winner gets all" type of game generally have problems like lengthy process to get the prize, trust issues etc. So, proud of being able to solve that problem because this project is fast, reliable, trustworthy and fully automated. And also Proud of being able to implement ChainLink VRF functionality and the Graph. Also it's deployed on Polygon Network, so the gas price will be very low and as the same time it's secure.

## What we learned
Learned about 
* how to use ChainLink VRF for randomness oriented problem
* the Graph api for catching on chain events and rendering them on front-end
* how to use external smart contract in solidity
* next.js framework with ether.js 
* implementation of web3modal
* setting up QuickNode provider
etc.

## What's next for Random Winner Game
There are couple of things that are next for this project e.g.
* Implementing multiple currencies as entry fees
* implementing NFTs as entry fees
* Deploying this project in multiple network
etc.
