# Decentralized_Voting
A decentralized voting app on the ethereum blockchain, using the truffle framework. (Built following tutorials from Dapp University.)

This app consists of a simple voting-client connected to a local ethereum blockchain.
- A voter can authenticate themselvs using their private key.
- When a voter votes, the smart contract performs a transaction on the blockchain and adds a vote to the election score.
- A vote can not be changed afterwards by the voter or anyone else. An attempt to cast a double vote will be rejected by the smart contract. The client-app also removes the voting-form after a vote has been cast.
- The voter is also "anonymous" in the sense that the only thing connected to the vote which can be found out by a third party is their ethereum wallet-address.

Dependencies:
    - Node Packet Manager (npm)
    - Truffle
    - Ganache
    - Meta Mask (chrome plugin)

To run this locally:
1. Make sure the dependencies are installed
2. Start Ganache
3. In the "Truffle"-directory, run "truffle migrate --reset" to reset the smart contract deployment
4. (Optional) Run "truffle test" to make sure all 5 tests in the testcripts returns successfully
5. Start the local server using "npm run dev" in the "truffle"-directory

The client application will now start on localhost:3000 (make sure you run this in chrome as you will need to use meta mask)

6. Create a new metamask account by choosing the "import account"-option and pasting the private key of one of the simulated addresses in Ganache (private keys can be found by clicking the key-symbol in the far right)
7. Refresh the page, and you should now be able to select a candidate to vote for.
8. You can import more accounts by repeating step 6 and vote with them as well to see that it affects the result.
