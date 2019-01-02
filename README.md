***
## Installation:
```
wget -q https://raw.githubusercontent.com/futureinvestcoin/mn_script/master/mn.sh
bash mn.sh
```
***

## Desktop wallet setup

After the MN is up and running, you need to configure the desktop wallet accordingly. Here are the steps for Windows Wallet
1. Open *Finc Core Wallet**.
2. Go to RECEIVE and create a New Address: **MN1**
3. Send **4000** **FINC** to **MN1**.
4. Wait for 15 confirmations.
5. Go to **Tools -> "Debug console - Console"**
6. Type the following command: **masternode outputs**
7. Go to  **Tools -> "Open Masternode Configuration File"**
8. Add the following entry:
```
Alias Address Privkey TxHash Output_index
```
* Alias: **MN1**
* Address: **VPS_IP:PORT**
* Privkey: **Masternode Private Key**
* TxHash: **First value from Step 6**
* Output index:  **Second value from Step 6**
9. Save and close the file.
10. Go to **Masternode Tab**. If you tab is not shown, please enable it from: **Settings - Options - Wallet - Show Masternodes Tab**
11. Click **Update status** to see your node. If it is not shown, close the wallet and start it again. Make sure the wallet is un
12. Select your MN and click **Start Alias** to start it.
***

## Usage:
```
finc-cli mnsync status
finc-cli getinfo
finc-cli masternode status #This command will show your masternode status
```

Also, if you want to check/start/stop **finc** , run one of the following commands as **root**:

```
systemctl status finc #To check the service is running.
systemctl start finc #To start finc service.
systemctl stop finc #To stop finc service.
systemctl is-enabled finc #To check whetether finc service is enabled on boot or not.
```
***

## Issues:
If your finc Core Wallet doesn't sync, go to **Tools -> Open Wallet Configuration File** and add the following entries:
```
addnode=185.178.47.147
addnode=185.178.47.148
addnode=46.229.214.66
addnode=176.53.160.211
addnode=185.178.47.216
addnode=185.178.46.2
addnode=185.178.47.251
addnode=185.178.47.226
addnode=185.178.47.225
addnode=185.178.46.170
addnode=185.178.46.229
```

