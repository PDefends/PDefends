# LM Hash Vulnerability Lab

This lab explores how LM (LAN Manager) hashes can be extracted and cracked, showing why they are considered insecure and deprecated in modern environments.

## Goals
- Understand what LM hashes are
- Simulate enabling LM hashes in a domain
- Extract LM hashes with `secretsdump`
- Crack the hash using `John the Ripper`

## Key Steps

### 1. Before LM Hashes Were Enabled
![Initial hash dump](./screenshots/1.PNG)

### 2. After Enabling LM Hashes via Group Policy
![Policy change](./screenshots/4.PNG)

### 3. Creating the `testuser` Account
![New user creation](./screenshots/7.PNG)

### 4. Cracking the Hash
![John the Ripper](./screenshots/9.PNG)

## Result
> Password for `testuser` was cracked in seconds: **ABC123!**

## What I Learned
At first, I was just following steps. But cracking the LM hash showed me how dangerous it is to leave this legacy setting enabled. LM hashes are weak and should never be used.
