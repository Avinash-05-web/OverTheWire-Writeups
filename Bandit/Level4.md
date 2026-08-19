# OverTheWire Bandit — Level 04 → Level 05

## 🎯 Objective

The password for the next level is stored in the only human-readable file inside the `inhere` directory.

## 🔎 Approach

I entered the `inhere` directory and needed to determine which file contained human-readable text.

I used the following command:

```bash
find . -type f | xargs file
```

This searched for files inside the directory and passed them to the `file` command.

The `file` command showed the type of each file. Among the results, I identified the file reported as **ASCII text**, meaning it was human-readable.

I then used `cat` on that file:

```bash
cat ./filexx
```

The file contained the password for the next level.

## 💻 Commands Used

```bash
cd inhere
find . -type f | xargs file
cat ./filexx
```

## 🧠 What I Learned

* How `find` can be used to locate files.
* How `xargs` can pass command output to another command.
* How the `file` command identifies the type and format of a file.
* ASCII text can be read directly using commands such as `cat`.

## 🚀 Key Takeaway

This level taught me how to identify a human-readable file among multiple files by checking their file types instead of opening each one manually.
