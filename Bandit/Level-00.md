# OverTheWire Bandit — Level 00 → Level 01

## 🎯 Objective
Level Goal

The goal of this level is for you to log into the game using SSH. The host to which you need to connect is bandit.labs.overthewire.org, on port 2220. The username is bandit0 and the password is bandit0. Once logged in, go to the Level 1 page to find out how to beat Level 1.

## 🔎 Approach
I first created a separate directory on my local system to keep the OverTheWire Bandit files and notes organized.

Next, I connected to the Bandit Level 0 server using SSH with the credentials provided by OverTheWire. I used the following command:

ssh -p 2220 bandit0@server-ip

When prompted, I entered the password provided for the bandit0 account.

After successfully authenticating, I was logged into the Bandit Level 0 environment and could begin exploring the challenge.
## 💻 Commands Used

```bash
ssh -p 2220 bandit0@<server-ip>
