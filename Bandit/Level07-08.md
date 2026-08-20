# OverTheWire Bandit — Level 07 → Level 08

## 🎯 Objective

The password for the next level is stored in the file `data.txt`, next to the word `millionth`.

## 🔎 Approach

I first logged into the Bandit Level 7 environment using the password obtained from the previous level.

After logging in, I used:

```bash id="3m8d1s"
ls -la
```

This displayed the files in the current directory, including a text file named:

```text id="f4q3b8"
data.txt
```

The file contained a large number of lines with different values, so manually searching through the entire file would not be efficient.

Since the objective specifically mentioned the word `millionth`, I used the `grep` command to search for that word inside `data.txt`:

```bash id="h2e5v9"
grep -i "millionth" data.txt
```

The command returned the line containing `millionth` along with the password next to it.

I used that password to successfully access **Bandit Level 8**.

## 💻 Commands Used

```bash id="v9j2kc"
ls -la
grep -i "millionth" data.txt
```

## 🧠 What I Learned

* How to use `ls -la` to view files, including hidden files and detailed file information.
* How to use `grep` to search for specific text inside a file.
* The `-i` option makes the search case-insensitive.
* Searching with `grep` is much more efficient than manually checking a large text file.

## 🚀 Key Takeaway

This level taught me how to efficiently search through large text files using `grep` when the information I need is associated with a specific keyword.
