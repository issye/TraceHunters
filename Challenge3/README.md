## 🚩 Challenge 3: The Encoded Heist (Final Exam)

**Files:**
* `evidence.jpg` (Intercepted image)
* `vault.zip` (Locked evidence container)

**Scenario:**
Congratulations, Agent. You have reached the final boss.

We have seized a digital vault (`vault.zip`) from the syndicate's server, but it is encrypted with a strong password. Brute-forcing it would take years.

However, we also intercepted an image (`evidence.jpg`) sent between two hackers just before the server went down. We believe the key is hidden inside this image. But be warned: these hackers are smart. They wouldn't send a password in plain English. They likely **encoded** it to look like random garbage so security scanners would miss it.

**Your Mission:**
1.  **The Interrogation:** Use `strings` to search the `evidence.jpg` file for a hidden "Access Key".
2.  **The Realization:** If you try to use the key you found, it will fail. Look closely at the text. Does it look like random letters ending with `=`?
3.  **The Decode:** Use your knowledge of **Base64** to decode that gibberish into the *real* password.
4.  **The Loot:** Unlock `vault.zip` and reveal the final flag.

**Hints:**
* *Filter your search! Use `strings evidence.jpg | grep "Key"`.*
* *If the text looks like `ZmxhZ3...`, it is Base64.*
* *To decode it in the terminal, use: `echo "YOUR_FOUND_KEY" | base64 -d`*

---

### 🏆 Workshop Conclusion

If you have solved all three challenges, you have successfully learned the core skills of a Forensic Analyst:
* [x] **Steganography:** Extracting hidden files (`binwalk`).
* [x] **File Repair:** Fixing corrupt binaries manually (`hexedit`).
* [x] **Data Extraction:** decoding hidden credentials (`strings` + `base64`).

**Welcome to the team, Hunter.**
