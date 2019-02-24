Connecting to testnet
==========================================================

First, follow the build instructions in [README](/README.md)

Then, to run cbtcd and connect to testnet

#### Linux
```
mkdir ~/.cbitcoin
touch ~/.cbitcoin/cbitcoin.conf
./src/cbtcd -testnet -gen
```

#### Windows
Click on Start/Windows Logo and type `cmd` once there type `start %AppData%\`. It will open the explorer in that directory. Create a new folder called "CBitcoin" and a text file. Open the text file and save as as `cbitcoin.conf` (be sure you remove the txt extension) in the directory. An empty file is sufficient

Create a Batch file in the CBTC directory called "start-wallet.bat" with the following:

```
echo "Starting the CBTC Wallet"
powershell -Command ".cbtcd.exe" -testnet -gen
@pause
```

Run start-wallet.bat and the blockchain will begin to be synced. After it is synced it will begin mining blocks. If you don't wish to mine remov the -gen option from the batch file.
Now that you have your node up you can use `cbtc-cli.exe` in cmd to make RPC calls to your node (i.e `cbtc-cli.exe -testnet getinfo`).
