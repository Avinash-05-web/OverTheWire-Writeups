# OverTheWire Bandit — Level 09 → Level 10

## 🎯 Objective

The password for the next level is stored in the file `data.txt`.

The password is contained within one of the few human-readable strings and is preceded by several `=` characters.

## 🔎 Approach

I first logged into the Bandit Level 9 environment and worked with the `data.txt` file.

The file contained mostly non-readable data, so I needed to extract the human-readable strings from it.

I used the `strings` command to extract readable text and piped its output to `grep` to search for lines containing `=` characters:

```bash
strings data.txt | grep "="
```

The command filtered the human-readable strings and displayed the entries containing `=`.

Among the results, I identified the string containing the password for the next level.

## 💻 Command Used

```bash
strings data.txt | grep "="
```

## 🧠 What I Learned

* How to use `strings` to extract human-readable text from files containing binary or non-readable data.
* How to combine commands using a pipe (`|`).
* How to use `grep` to filter output based on a specific character or pattern.
* How combining simple Linux commands can make it easier to locate specific information.

## 🚀 Key Takeaway

This level taught me how to extract readable information from a file containing non-readable data and then filter the results using `grep` to quickly locate the required information.
