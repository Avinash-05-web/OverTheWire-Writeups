# OverTheWire Bandit — Level 00 → Level 01

## 🎯 Objective
Level Goal

The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

## Commands you may need to solve this level
ls , cd , cat , file , du , find
## 🔎 Approach

I first created a separate directory on my local machine to keep my OverTheWire write-ups organized.

I then connected to the Bandit server using SSH with the `bandit0` account:

```bash
ssh -p 2220 bandit0@bandit.labs.overthewire.org
```

After successfully logging in, I checked the files available in the current directory and found a file named `readme`.

I used the `cat` command to display the contents of the file:

```bash
cat readme
```

The file contained the password required for the next level, `bandit1`.

After obtaining the password, I exited the `bandit0` session and returned to my local machine:

```bash
exit
```

I then connected to the server again, this time using `bandit1` as the username:

```bash
ssh -p 2220 bandit1@bandit.labs.overthewire.org
```

When prompted for the password, I entered the password obtained from the `readme` file.

This successfully logged me into **Bandit Level 1**.

## 💻 Commands Used

```bash
ssh -p 2220 bandit0@bandit.labs.overthewire.org
cat readme
exit
ssh -p 2220 bandit1@bandit.labs.overthewire.org
```

## 🧠 What I Learned

* How to connect to a remote Linux server using SSH.
* How to inspect files in the current directory.
* How to use `cat` to read the contents of a text file.
* How credentials can be stored inside files in a Linux environment.
* How to exit an SSH session and reconnect using a different user account.

## 🚀 Key Takeaway

This level introduced the basic workflow of the Bandit wargame: connect to a level, investigate the environment, find the required credential, and use it to authenticate to the next level.
