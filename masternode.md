# Empire Coin Masternode Install Guide

Launch an Ubuntu 16.04 server from either Vultr or DigitalOcean
Login to your newly launched server
Copy and paste the following line into the server:
wget https://github.com/EmpireCryptoNetwork/emp/releases/download/1.0/emp-mn.sh -O emp-mn.sh
chmod +x emp-mn.sh
./emp-mn.sh

Open your wallet debug console:
Tools -> Debug Console

Type the following to generate a new address:
getaccountaddress mn1 or what masternode number it is that you're launching

Send exactly 1,000 EMP to this newly generated address
Go to the debug console and enter:
masternode genkey - this is your private key for masternode installation

Go back to your VPS and follow the instructions

Go back to your wallet debug console and type:
masternode outputs

Next, click on:
Tools -> Open Masternode Configuration File

You will receive your IP address of the VPS after installation is complete along with the private key again, enter the MN config like this below:
mn# IP_ADDRESS:14321 PRIVATE_KEY TXID INDEX

The TXID and INDEX came from the masternode outputs command
Save the file, restart the wallet, and start the masternode after 16 confirmations!
