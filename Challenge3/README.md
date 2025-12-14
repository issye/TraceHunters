## 🚩 Challenge 3: The Scrambled Cat 

**Files:** `part_1.dat`, `part_2.dat`, `part_3.dat`

**The Story:**
We attempted to download this high-priority evidence from the suspect's server, but the connection was interrupted. The file—which we believe is a photo of the mastermind's cat—arrived in **three broken pieces**.

Currently, the cat is in a state of quantum superposition: it is neither alive nor dead, it is just... data chunks.

**Your Mission:**
1.  **Analyze the Anatomy:** Use `hexedit` to identify the body parts.
    * Which part is the **Head**? (Look for the PNG Signature `89 50...`)
    * Which part is the **Tail**? (Look for the `IEND` tag at the bottom)
    * Which part is the **Body**? (The piece with neither)
2.  **Perform the Surgery:** You must stitch the file back together.
3.  **The Ultimate Pun:** To fix this file, you must use the Linux **`cat`** command.
    * *Literally. You have to `cat` the cat.*

**Hints:**
* *Command syntax: `cat [HEAD_FILE] [BODY_FILE] [TAIL_FILE] > fixed_cat.png`*
* *If you do it right, the image will open. If you do it wrong, the cat will look... very strange.*
