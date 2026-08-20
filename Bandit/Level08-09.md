# OverTheWire Bandit — Level 08 → Level 09

## 🎯 Objective

The password for the next level is stored in the file `data.txt`.

The password is the **only line of text that occurs exactly once** in the file.

## 🔎 Approach

I first logged into the Bandit Level 8 environment and worked with the `data.txt` file.

The file contained many lines of text, including repeated values. The objective was to identify the line that occurred only once.

I used the following command:

```bash
sort data.txt | uniq -c
```

The `sort` command sorted the contents of `data.txt`, placing identical lines next to each other.

The output was then passed to `uniq -c`, which counted how many times each unique line occurred.

By checking the output, I identified the line with a count of `1`. That line contained the password for the next level.

## 💻 Command Used

```bash
sort data.txt | uniq -c
```

## 🧠 What I Learned

* How to sort the contents of a file using `sort`.
* How to use pipes (`|`) to pass the output of one command to another.
* How `uniq -c` counts repeated lines.
* Why sorting is useful before using `uniq`.
* How command combinations can make searching through large files more efficient.

## 🚀 Key Takeaway

This level taught me how to combine multiple Linux commands using a pipe to identify unique data efficiently. `sort` organizes the data, while `uniq -c` makes it easy to identify how frequently each line occurs.
