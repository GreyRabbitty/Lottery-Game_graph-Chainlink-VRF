# https://lottery-game-graph-chainlink-vrf.vercel.app/

## Requirements 
install `node` in your system

## Instruction on how to run this Project 
```
cd interface
nom install
npm run dev
```
or
```
cd interface
yarn
yarn dev
```
## Rules and Description
In this game, there are two type of parties e.g. the host and the player. Host is the deployer of smart contract. Only the host can host a game. The host has the power to determine entry fees (which a player have to pay to play the game) and number of maximum players to participate. The players have to pay the fees that the host determined to enter the game. After all the players joining, the smart contract will randomly choose a winner using ChainLink VRF among the player. The winner will get all the fees that the other players submitted at the beginning of the game (including winners fees too). The results will be shown with the game id and winner's wallet address. There are some important criteria of this DApp. 1. There will be always 1 game at a time. The host cannot host multiple game at a time. To host 2nd game , the 1st game have to be finished. 2. The game will not ended unless all the players are joined which was determined by the host at the beginning of the game and also pay the entry fees that was also determined at the beginning of the game. 3. Each player also have to pay 1 Link to play the game. 
