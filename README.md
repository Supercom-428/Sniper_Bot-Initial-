# Sniper_Bot-Initial-

Build a snipe bot to monitor and trade liquidity pairs

The snipe trading bot will perform the following functions:

* First the Python process listens to Uniswap events for newly created token pairs
* Then the system identifies and process new token pairs
* Finally the bot submits a transaction to buy the new token using a smart contract

After the bot identifies a newly created liquidity pair send a transaction to the smart contract to execute a token swap.

Integrate into the snipe trading bot
To complete this bot you will need to integrate the steps below into the Python code above.

Looking at the Uniswap Liquidity Pair Creation Log screen print above. You will need to save token0, token1 and the pair address as return values in your code. You will need these values to perform a token swap.
Determine which address is the new token address. Most pairs are setup with WETH vs New Token.
Read this tutorial on how to send an ETH transaction to the blockchain using Web3.py in Python
Using the new token address (token0, token1) call the function getAmountOutMin in the smart contract from the Python code. This will return the amountOutMin which is needed as an input for the swap.
Use the return value from getAmountOutMin and call the function swap in the smart contract from the Python code.
After finishing these steps you have a working snipe trading bot that monitors and trades liquidity pairs.

The Solidity smart contract can be modified to support sniping tokens on other Uniswap clone exchanges. As an example the Binance Smart Chain, Polygon, Ubiq, CheapEth, Fantom are Ethereum blockchain clones. Each blockchain has a copy of the Uniswap decentralized exchange. Consider adding the decentralized exchanges below to your snipe bot.

Uniswap
Mooniswap
1Inch Exchange
Sushiswap
Sashimiswap
Binance Smart Chain Pancake Swap
CheapEth CheapSwap
Ubiq Shinobi
Polygon SwapMatic

This code is for learning and entertainment purposes only. This code has not been audited and use at your own risk. Remember smart contracts are experimental and could contain bugs.
