## OverTheWire Bandit — Level 00 → Level 01

## 🎯 Objective
Level Goal

The password for the next level is stored in a file called - located in the home directory
## Commands you may need to solve this level
ls , cd , cat , file , du , find
## 🔎 Approach

I logged into the Bandit server as `bandit1` using the password obtained from the previous level.

After logging in, I checked the files in the current directory and found a file named:

```text id="qqjv8h"
-
```

The filename `-` is special because many Linux commands interpret `-` as an option or standard input rather than as a normal filename.

To explicitly tell `cat` that I wanted to read the file named `-` from the current directory, I used:

```bash id="9k9tq5"
cat ./-
```

The command successfully displayed the password for the next level.

## 💻 Command Used

```bash id="v9by9f"
cat ./-
```

## 🧠 What I Learned

* Linux filenames can contain special characters.
* A filename consisting of `-` can be interpreted differently by command-line tools.
* Using `./` explicitly refers to a file in the current directory.
* `cat ./-` can be used to read a file literally named `-`.

## 🚀 Key Takeaway

This level taught me that filenames can sometimes conflict with command-line conventions. Using `./` is a simple way to clearly specify that `-` is a filename rather than a command option.
