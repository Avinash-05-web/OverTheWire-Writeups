# OverTheWire Bandit — Level 06 → Level 07

## 🎯 Objective

The password for the next level is stored somewhere on the server.

The file has all of the following properties:

* Owned by user `bandit7`
* Owned by group `bandit6`
* Exactly 33 bytes in size

## 🔎 Approach

I first logged into the Bandit server using the password obtained from the previous level.

Since the password could be located anywhere on the server, I needed to search from the root directory.

I used the `find` command with the given ownership and file-size conditions:

```bash
find / -type f -user bandit7 -group bandit6 -size 33c
```

The command searched the entire filesystem for a regular file that:

* Is owned by `bandit7`
* Belongs to the `bandit6` group
* Has a size of exactly 33 bytes

While searching, the command returned several `Permission denied` messages for directories that the `bandit6` user could not access.

Among the results, I found the required file at:

```text
/var/lib/dpkg/info/bandit7.password
```

I then used `cat` to read the contents of the file:

```bash
cat /var/lib/dpkg/info/bandit7.password
```

The file contained the password for the next level.

## 💻 Commands Used

```bash
find / -type f -user bandit7 -group bandit6 -size 33c
cat /var/lib/dpkg/info/bandit7.password
```

## 🧠 What I Learned

* How to search the entire Linux filesystem using `find /`.
* How to search for files based on their owner using `-user`.
* How to search based on group ownership using `-group`.
* How to search for files with an exact size using `-size 33c`.
* How permission restrictions can produce `Permission denied` messages during filesystem searches.
* How multiple conditions can be combined in a single `find` command.

## 🚀 Key Takeaway

This level taught me how file ownership, group ownership, and file size can be combined as search criteria to locate a specific file on a Linux system.
