# OverTheWire: Bandit Level 0 Guide

Welcome to my guide for the Bandit Level 0 of the OverTheWire wargames.

## Task

Your task is to gain access to the game server using the following credentials:

- **Server:** `bandit.labs.overthewire.org`
- **Port:** `2220`
- **Username:** `bandit0`
- **Password:** `bandit0`

## Solution

To connect to the server, you will use an SSH client. The standard command structure for the SSH command at this level is as follows:

```bash
ssh username@server -p port
Note: Replace <username>, <server>, and <port> with the provided credentials. The -p flag is used to specify the port number.

For our purposes, the command translates to:
ssh bandit0@bandit.labs.overthewire.org -p 2220

When you run the command, you'll be prompted to enter the password. Input the provided password (it will not be visible as you type due to security reasons).

Congratulations, you've completed Level 0!
