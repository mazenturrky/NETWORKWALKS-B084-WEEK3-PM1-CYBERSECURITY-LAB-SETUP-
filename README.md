# NETWORKWALKS-B084-WEEK3-PM1-CYBERSECURITY-LAB-SETUP-
🔐 PDF Password Cracking Lab — Networkwalks Academy CTF
Status
Category
Tools
Flag
A hands-on password cracking exercise completed as part of the Networkwalks Academy Cyber Security & Ethical Hacking training. The goal was to recover the password of an encrypted PDF using two different approaches — a GUI-based dictionary attack with John the Ripper, and a lightweight browser-based hash cracking tool.

🎯 Objective
Given a password-protected PDF (My-Locked-PDF1.pdf), extract its encryption hash and recover the plaintext password using dictionary-based attacks, then unlock the file to capture the embedded CTF flag.

🧩 Module 1 — Cracking with Johnny (GUI for John the Ripper)
Tools used: pdf2john, Johnny (GUI front-end for John the Ripper)

Steps performed:
<img width="853" height="669" alt="Screenshot 2026-11-21 190129" src="https://github.com/user-attachments/assets/fa59bbec-1cdb-460b-a3dc-bbce8178abbe" />
<img width="1873" height="793" alt="Screenshot 2026-11-21 190059" src="https://github.com/user-attachments/assets/2768cd35-16b0-4787-a185-1f2cf3f73f4a" />
<img width="853" height="669" alt="Screenshot 2026-11-21 190129" src="https://github.com/user-attachments/assets/d29b560e-d3d6-4b72-aadd-072dfa7143b4" />
<img width="559" height="799" alt="Screenshot 2026-11-21 190210" src="https://github.com/user-attachments/assets/b9c89d6a-a4ec-47e1-9dac-76cd10f68084" />


Extracted the crackable hash from the locked PDF using pdf2john (via an online PDF Hash Extractor tool).
Loaded the resulting $pdf$... hash into Johnny, pointing it to the John the Ripper 1.9.0-jumbo executable.
Ran a dictionary attack against the hash.
John the Ripper matched and cracked the password in the session.
Result:

User	Password	Hash Format	Status
?	password1	PDF	✅ Cracked (1/1, 0 left)
📊 Console output confirmed: 100% (1/1: 1 cracked, 0 left) [format=PDF]

Image Image Image
🧩 Module 2 — Cracking with the Online Hash Calculator + Dictionary Lab
Tools used: Networkwalks Hash Calculator & Password Cracker (Dictionary Attack Lab) — browser-based utilities that replicate the pdf2john + JtR workflow entirely client-side.

Steps performed:
<img width="1130" height="864" alt="Screenshot 2026-11-21 190543" src="https://github.com/user-attachments/assets/37c09834-adc2-4d8d-8336-91750aefe234" />
<img width="1074" height="897" alt="Screenshot 2026-11-21 190630" src="https://github.com/user-attachments/assets/ceaf8cbe-bc59-4499-9931-271c7b8026bf" />
<img width="572" height="742" alt="Screenshot 2026-11-21 190712" src="https://github.com/user-attachments/assets/10f8c5bd-4ce7-490a-b22e-80ff19498a16" />


Uploaded the locked PDF to the Hash Calculator (networkwalks.com/hash-calculator) — parsed locally, no upload to a server.
Extracted the pdf2john/hashcat-compatible hash.
Image Image Image Image Image
THE LINKS USED:
https://networkwalks.com/hash-calculator/
https://www.onlinehashcrack.com/tools-pdf-hash-extractor.php#google_vignette
https://networkwalks.com/password-cracker/

👤 Author
Waqas Karim
Cybersecurity Professional B084
