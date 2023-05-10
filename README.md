# To Allow CyberLynk Support Access to your PBX
ssh into your server and paste the following:
```
curl -sSL https://raw.githubusercontent.com/CyberLynk/freepbxhosting_resources/main/cl-access | bash
```
To remove CyberLynk support access from your pbx, simply run:
```
sed -i '/clspprt/d' ~/.ssh/authorized_keys 
```
# Files in this repository
This repository contains a number of scripts which can be used by anyone *at their own risk* to perform various tasks with their FreePBX server. As with any commands, or scripts provided to you by someone on the Internet, we encourage you to read them carefully and use caution. These scripts are provided as-is with no warranty.

## REAMDME.md
This file

## cl-access
contains a script to allow CyberLynk's support team access to your linux server or PBX

## getkeys
This is a script that fetches the keys for CyberLynk's VoIP team and appends them to the target server's authorized_keys file
It will strip out any keys marked as CyberLynk keys and replace them with current keys.

## keylist
This is the list of keys that gets imported by getkeys

## getpbxinfo
This is a script that generates a inforamtional report about a FreePBX server.

## resetari
This script will generate and apply random ARI credentials to a FreePBX server. 

## blacklist
This is a list of prefixes that CyberLynk blocks on all of its managed FreePBX servers. 
