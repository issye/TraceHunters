
````markdown
# 🕵️ Trace Hunters: Introduction to Forensics

Welcome to the **Trace Hunters** workshop! This repository contains the challenge files you will need for our hands-on session.

Today, you will learn how to:
1.  **Look beyond the interface:** Don't trust file icons or extensions.
2.  **Analyze binaries:** Use tools to see the raw data.
3.  **Repair corruption:** Manually fix broken files to recover evidence.

---

## 🛠️ Prerequisites & Installation

Before starting, ensure you have the necessary tools installed on your Linux machine (Kali, Ubuntu, etc.).

Open your terminal and run:

```bash
sudo apt update && sudo apt install binwalk hexedit unzip -y
````

### The Toolkit

  * **`file`**: Identifies the true file type.
  * **`binwalk`**: Scans for hidden files (embedded data).
  * **`strings`**: Extracts readable text from binary files.
  * **`hexedit`**: Allows you to view and edit the raw bytes of a file.

-----

## 🚩 Challenge 1: Meme-Ception

**File:** `challenge1.jpg`

**Scenario:**
We intercepted this image from a suspect's computer. It looks like a normal meme, but our intelligence suggests there is secret data hidden inside it. We believe the data is locked, but the suspect might have been careless with the key.

**Objective:**

1.  Find the hidden file inside the image.
2.  Extract it.
3.  Find the password to unlock it and reveal the flag.

**Hints:**

  * *Is the image hiding an archive inside?*
  * *If the extracted file is locked, check the original image for "strings" that look like passwords.*

-----

## 🚩 Challenge 2: The Deceptive Zombie

**File:** `flag.txt`

**Scenario:**
We recovered this file from a damaged hard drive. It is named `flag.txt`, but when we try to read it, it just shows garbage data. The operating system doesn't know how to open it because the "Magic Bytes" (Header) are missing.

**Objective:**

1.  Identify what the file *should* be (Look for internal clues like `IHDR`).
2.  Use a Hex Editor to repair the file header.
3.  Rename the file and open it to get the flag.

**Hints:**

  * *The extension `.txt` is a lie.*
  * *Open it in `hexedit`. If the first bytes are `00 00...`, the file has no identity.*
  * *Can you restore the signature for a PNG image?*

-----

## 🆘 Cheat Sheet (Magic Bytes)

If you need to repair a file header, use these signatures:

| File Type | Hex Signature (Start of file) |
| :--- | :--- |
| **PNG Image** | `89 50 4E 47 0D 0A 1A 0A` |
| **JPEG Image** | `FF D8 FF E0` |
| **ZIP File** | `50 4B 03 04` |
| **PDF Doc** | `25 50 44 46` |

Good luck, Hunters\!

```
```
