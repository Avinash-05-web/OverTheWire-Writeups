# OverTheWire Bandit — Level 05 → Level 06

## 🎯 Objective

The password for the next level is stored somewhere under the `inhere` directory.

The required file has these properties:

* Human-readable
* Exactly 1033 bytes in size
* Not executable

## 🔎 Approach

I entered the `inhere` directory and needed to search through the files based on the conditions given in the level.

I used the `find` command to search for a file with the required size and exclude executable files:

```bash
find . -type f -size 1033c ! -executable
```

The command returned the file:

```text
./maybehere07/.file2
```

I then used `cat` to read the file:

```bash
cat ./maybehere07/.file2
```

The contents of the file contained the password for the next level.

## 💻 Commands Used

```bash
find . -type f -size 1033c ! -executable
cat ./maybehere07/.file2
```

## 🧠 What I Learned

* How to search recursively through directories using `find`.
* How to search for files based on their exact size.
* How to exclude executable files using `! -executable`.
* How multiple conditions can be combined in a `find` command.
* How hidden files can still be located using command-line tools.

## 🚀 Key Takeaway

This level taught me how to use multiple search conditions with `find` to efficiently locate a specific file instead of manually checking every file in a directory.
