# OverTheWire Bandit — Level 11 → Level 12

## 🎯 Objective

The password for the next level is stored in the file `data.txt`.

All lowercase and uppercase letters in the file have been rotated by 13 positions, which is known as **ROT13**.

## 🔎 Approach

I first checked the contents of `data.txt` and found that the text was not immediately readable.

Since the level stated that the letters had been rotated by 13 positions, I identified the encoding as **ROT13**.

I copied the encoded message from `data.txt` and used **CyberChef** to decode it using the ROT13 operation.

After applying ROT13, the message became readable and revealed the password for the next level.

## 💻 Commands Used

I first viewed the contents of the file:

```bash id="y9b6c4"
cat data.txt
```

I then copied the encoded message and decoded it using CyberChef with the **ROT13** operation.

## 🧠 What I Learned

* ROT13 is a letter substitution technique that rotates each letter by 13 positions.
* ROT13 works on both uppercase and lowercase letters.
* Since the alphabet contains 26 letters, applying ROT13 twice returns the original text.
* CyberChef can be used to quickly decode and analyze encoded data.
* Recognizing the encoding technique is an important part of solving cybersecurity challenges.

## 🚀 Key Takeaway

This level taught me how to recognize ROT13-encoded text and decode it using CyberChef. It also showed the importance of identifying the type of encoding before attempting to decode a message.
