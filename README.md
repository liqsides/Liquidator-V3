# Liquidator-V3
A liquidator script for the QIDAO protocol on the Polygon network

## Improvements
With V3, we add the asyncio library to run coruotines and increase the speed of our liquidator. There has also been certain liqLoop() bug fixes, such as it trying to pop from the dict it is looping through, casuing only one liq tx per loop. Added some safeguards to keep gas reasonable, making sure neither gas nor safe_gas exceed 2000 gwei.

## Set Up
Similar to V2, you will need to create your own Python3 environment and pip install web3 to have your environment ready. Then, you will need to fill out the url variable with a MATIC RPC endpoint, myAddress variable with your wallet address and priv variable with your wallet private key. The script will first scan the vaults and build up data about them, then will begin scanning for liquidations. All you need to do is hold some MAI in your wallet and you have a small chance at some liquidations.

## Considerations
If I am posting a liquidator script, it likely means I have already developed one much faster. As such I do not expect this script to be competitive with newer scripts I have made and may even lose money on failed transactions. Also, the derisk function has lacked thorough testing as I had some bugs that prevented me from testing the function at all and I have forked to a different copy since. The purpose of derisk is to swap 50% of your MATIC back for MAI once your wallet holds over 50 MATIC. This script is only valid on MATIC vaults, it will not work on camWMATIC vaults without some alteration.

## Help Me Out
I accept payments on both MATIC and ETH networks, thank you frens <3

0xe0f1F6d9b57DB098a1c786a835A55A1Ff64d39EE
