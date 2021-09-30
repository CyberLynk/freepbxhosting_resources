# freepbxhosting_resources
This repository is a collection of various resources for use with freepbxhosting.com services.

## **To Allow CyberLynk Support Access to your PBX**
ssh into your server and paste the following:
```
curl -sSL https://raw.githubusercontent.com/CyberLynk/freepbxhosting_resources/main/cl-access | bash
```
To remove CyberLynk support acces from your pbx, simply run:
```
sed -i '/clspprt/d' ~/.ssh/authorized_keys 
```
# Key Files

## REAMDME.md
This file

## cl-access
contains a script to allow CyberLynk's support team access to your linux server or PBX

## getkeys
This is a script that fetches the keys for CyberLynk's VoIP team and appends them to the target server's authorized_keys file
It will strip out any keys marked as CyberLynk keys and replace them with current keys.

## keylist
This is the list of keys that gets imported by getkeys
