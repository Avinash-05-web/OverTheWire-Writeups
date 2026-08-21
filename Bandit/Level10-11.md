# OverTheWire Bandit — Level 10 → Level 11

## 🎯 Objective

The password for the next level is stored in the file `data.txt`.

The contents of the file are Base64 encoded.

## 🔎 Approach

I first checked that the `data.txt` file was present in the current directory.

I then used the `base64` command with the `-d` option to decode the contents of the file:

```bash id="9y2k8p"
base64 -d data.txt
```

The command decoded the Base64-encoded data and displayed the password for the next level.

## 💻 Commands Used

```bash id="kl2l6v"
ls
base64 -d data.txt
```

## 🧠 What I Learned

* How Base64 encoding is used to represent data as text.
* How to decode Base64 data using the Linux `base64` command.
* The `-d` option tells `base64` to decode the input.
* How command-line tools can quickly decode encoded information.

## 🚀 Key Takeaway

This level introduced me to Base64 decoding and showed how the Linux `base64` utility can be used to recover readable information from encoded data.
