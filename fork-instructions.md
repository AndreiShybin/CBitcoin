
# Instructions to set up a ClassicBitcoin full-node to Mine the Fork
Linux ONLY, 500GB+ recommended

*You will not receive a mining reward if you choose to help mine the fork*

**Classic Bitcoin**

March 2, 2018

#

**Install Classic Bitcoin**

Follow the instructions [here](https://github.com/CBitcoin/ClassicBitcoin/blob/master/README.md).

**Download + Decompress Snapshot Data (BTC UTXOs)**
```
cd ~/.cbitcoin/
Download CBTC Fork UTXO.
https://drive.google.com/open?id=1zUZB06NzLbVvee_KEn3TqAZfEh-GlQMQ | tar xvz
A folder named utxo_snapshot containing CBTC UTXO Data is expected in the coin Data Directory.



curl https://s3.amazonaws.com/cbtc.snapshot/utxo_snapshot.tar.gz | tar xvz
```

You can also generate the utxo_snapshot yourself [here](https://github.com/CBitcoin/utxo_dump).

**Make the config file**
```
mkdir ~/.cbitcoin
touch ~/.cbitcoin/cbitcoin.conf
```

**Run the daemon**
```
cd ~/ClassicBitcoin
./src/cbtcd
```
