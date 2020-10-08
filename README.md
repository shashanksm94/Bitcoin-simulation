# Bitcoin Simulation
 \
<b>Teammates:</b> Shashank Mayekar, Tanya Pathak \
\
<b>Youtube video at:</b> https://youtu.be/AZLhvqB13xM \
\
<b>Working functionality:</b>
* Wallets (Every node is a wallet with a public-private key pair and a derivable public address.
* Genesis block mining
* Bitcoin Transactions (Starting from first miner)
* Coinbase transaction (Rewards)
* Node gets interrupted when someone else broadcasts a mined block of same height
* Unspent transaction outputs for each wallet (UTXO model) 
* Change transaction as part of UTXO (in tx outputs)
* Computing balance of wallet from its UTXOs
* Multiple inputs and multiple outputs for transactions
* Digitally signing a transaction using private key
* Verifying a signed transaction using signer’s public key
* Distributed protocol:
* Network can handle 100+ nodes and as many miners
* Distributed transaction pool for new broadcasted transactions at each node
* 16 transactions execute (creating 16 blocks; # transactions can be increased)
* Implemented Phoenix application
* Created chart – Bitcoins transacted(http://localhost:4000/bitcoinBtc)
* Created chart – Hashes computed to mine (http://localhost:4000/bitcoinHash)
* Created chart – Transactions in block (http://localhost:4000/bitcoinTx)
* Created list –Transactions broadcasted (http://localhost:4000/bitcoinTxList)
 
<b>Steps to run the project:</b> \
The main bitcoin program initiates from within the Phoenix ‘Application.ex’. \
We pass 100 as the number of nodes, and 80 as number of miners among them to Btcmain GenServer. \
 \
<b>Main components:</b>
* node.ex corresponds to each node in the network.
* wallet.ex corresponds to the wallet of each node.
* proj42.ex is the main component program which creates nodes
* btcmain.ex invokes proj42.ex, executes transactions, and monitors the network
 \
 \
<b>To compile the project, do:</b>
* cd into project directory (bitcoin1)
* mix compile
 \
 \
<b>To start your Phoenix server:</b>
* Install dependencies with `mix deps.get`
* Create and migrate your database with `mix ecto.setup`
* Install Node.js dependencies with `cd assets && npm install`
* Start Phoenix endpoint with `mix phx.server`
Now you can visit [`localhost:4000`](http://localhost:4000) from your browser.
\
\
<b>Open 4 pages on the browser:</b>
* http://localhost:4000/bitcoinBtc
* http://localhost:4000/bitcoinHash
* http://localhost:4000/bitcoinTx
* http://localhost:4000/bitcoinTxList
\
\
The program will begin running. \
The 4 pages will keep updating (Need to refresh if they don't) \
The program output is also visible in the cmd (information on blocks, transactions and balances of nodes involved in transactions). \
Around 16 blocks will be mined. \
