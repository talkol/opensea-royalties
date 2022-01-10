# OpenSea Royalties

A simple script to extract NFT sales on OpenSea. The script does not rely on OpenSea's off-chain databases which may contain incorrect data. Instead, the script extracts the sales data from Ethereum mainnet on-chain events. The script goes over every transfer executed by the NFT contract (by querying transfer events) and for each checks if the transfer was conducted due to an OpenSea Ethereum mainnet sale. If so, the script outputs the sale price in ETH. Please note that many transfers may not be related to a sale, for example when an NFT owner transfers the asset between two of their wallets, we would still see a transfer in the output.

## Instructions

1. Make sure you have Node.js installed and run in terminal:
    ```
    npm install
    ```

2. Go over the code (royalties.js) and review all the TODOs

3. Run in terminal:
    ```
    node . > output.csv
    ```

4. Open `output.csv` in Excel