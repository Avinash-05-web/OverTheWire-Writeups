# OverTheWire Bandit — Level 02 → Level 03

## 🎯 Objective

The password for the next level is stored in a file named `--spaces in this filename--` located in the home directory.

## 🔎 Approach

I first used the `ls` command to check the files available in the current directory:

```bash
ls
```

The output showed a file named:

```text
--spaces in this filename--
```

Because the filename contains spaces and begins with `--`, directly using `cat` with the filename could cause it to be interpreted as command-line options.

To explicitly specify the file in the current directory, I used:

```bash
cat "./--spaces in this filename--"
```

This successfully displayed the password for the next level.

## 💻 Commands Used

```bash
ls
cat "./--spaces in this filename--"
```

## 🧠 What I Learned

* How to use `ls` to inspect files in a directory.
* How spaces in filenames can affect command-line commands.
* How quotation marks can preserve spaces as part of a filename.
* How `./` explicitly refers to a file in the current directory.
* How filenames beginning with `--` can be confused with command-line options.

## 🚀 Key Takeaway

This level taught me how to correctly work with filenames containing spaces and special characters. Using quotes together with `./` allowed me to reference the exact filename without the shell or command interpreting its contents incorrectly.
