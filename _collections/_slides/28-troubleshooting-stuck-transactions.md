--- 
title: "Troubleshooting Stuck Transactions"
slideId: "troubleshooting-stuck-transactions"
type : custom     
notes : |
    <p>A nonce is an added variable that is used to prevent double spending by keeping your transactions ordered. Each transaction per wallet has a unique nonce used to keep this order. If someone was to send their entire wallet balance containing one ether with a low gas fee, and then tries to send that same amount with a higher gas fee, the nonce is the variable assigned to transactions that makes sure they are executed in order, avoiding a double-spend scenario.</p>
    <p>For each transaction conducted with that wallet, the nonce increases by exactly one. It does not skip a number. The transaction with a higher nonce cannot be processed before a transaction with a lower nonce. The practical effect is that these transactions must occur in order. If one gets stuck, the others do too. This must be done in order to avoid double spending. In order to speed up or cancel a transaction, we need to learn how to clear or modify a nonce. But first, we need to know where to find this information.</p>
    <p>Metamask keeps track of every single transaction conducted using the wallet, which can be especially useful in troubleshooting. If you are confused about the status of your transaction, you have a couple of options:</p>
    <ul><li>Use the three dots on the main wallet page to select “view account on Etherscan”. This will take you to a block explorer page that has an overview of all your account activity</li>
    <li>If you are looking to troubleshoot a specific transaction, select it from your transaction history and select “view transaction on Etherscan”</li>
    <li>If you are trying to speed up or cancel a transaction, make sure to note the nonce of the stuck transaction. It must be modified in order for the transaction to become unstuck</li></ul>
    <p>Alternately, you can go straight to a block explorer and enter in your account information, and select the transaction in question. This adds an extra step, but it’s good to know. Block explorers are searchable by address, transaction hash, or block number.</p>
    <p>Sometimes your transaction will get stuck because there was a rapid increase in gas price. Basically, your transaction is in limbo until a miner decides to include it in a block. Your transaction might never get processed if gas prices sustain its increased price. Since you have one stuck transaction, any successive transaction from the same wallet cannot go through. This provision is used to prevent double-spending, and effectively works by numbering the order of the transactions from your wallet. This is the purpose that a nonce serves, a basic order of transactions. To unstick our transaction, we need to reorder the transactions coming from our wallet in order to increase the gas provided to execute the original transaction. To do this we must manually change the nonce of our second transaction:</p>
    <ul><li>Go to your account icon</li>
    <li>Click Settings</li>
    <li>Choose advanced settings</li>
    <li>Enable customizable nonce, allowing us to reorder our wallet’s transactions</li></ul>
    <p>Now when you send a transaction, a field will appear, allowing you to enter a specific nonce. To unstick a transaction, send a very small amount of Eth with the same nonce that is found on the pending transactions using a block explorer. Your transaction with the custom nonce will be processed along with your original transaction, effectively adding gas to the stuck transaction.</p>
bodyText : <iframe> width="1366" height="528" src="https://www.youtube.com/embed/uSp9AcozWro" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
---
