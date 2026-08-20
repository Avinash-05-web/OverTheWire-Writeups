# OverTheWire Bandit — Level 03 → Level 04

## 🎯 Objective

The password for the next level is stored in a hidden file inside the `inhere` directory.

## 🔎 Approach

I first checked the contents of the current directory to confirm that the `inhere` directory was present.

I then entered the directory using:

```bash
cd inhere
```

After entering the directory, I used `ls` to list its contents.

The normal `ls` output did not show the hidden file, so I needed to identify the hidden file containing the password.

After locating the hidden file named `...Hiding-From-You`, I used `cat` to read its contents:

```bash
cat ...Hiding-From-You
```

The command displayed the password for the next level.

## 💻 Commands Used

```bash
cd inhere
ls
cat ...Hiding-From-You
```

## 🧠 What I Learned

* How to navigate into a directory using `cd`.
* How to inspect directory contents using `ls`.
* Hidden files are not normally displayed by a basic `ls` command.
* How to read a file using `cat`.

## 🚀 Key Takeaway

This level introduced the concept of hidden files in Linux and showed that a normal directory listing may not reveal every file present.
