Linux AES-256 File Encryption & Decryption Demo.

  Overview
A beginner-friendly hands-on project demonstrating symmetric encryption using OpenSSL on Linux.  
I encrypted a plaintext message, verified it became unreadable, securely deleted the original, then decrypted it back to the original form.

Technologies Used
- Linux terminal (Ubuntu / any distro)
- OpenSSL (AES-256-CBC with salt)
- Basic commands: echo, cat, rm, ls

Project Steps
1. Created plaintext file: `echo "Encryption hides data but does not make systems secure." > message.txt`
2. Encrypted: `openssl enc -aes-256-cbc -salt -in message.txt -out message.enc`
3. Verified encrypted file is unreadable: `cat message.enc` → binary garbage
4. Deleted original: `rm message.txt`
5. Decrypted: `openssl enc -d -aes-256-cbc -in message.enc -out message_decrypted.txt`
6. Verified: `cat message_decrypted.txt` → original message restored

Key Learning Outcomes
- Understood symmetric encryption basics (AES-256-CBC)
- Learned importance of secure key management (passwords)
- Practiced secure file handling in Linux
- Realized encryption protects data at rest but not against weak passwords or system compromise

Why It Matters
This project highlights foundational cybersecurity concepts: protecting confidentiality with encryption while understanding its limitations.

Screenshots
![Encryption output](screenshot-encrypt.png)
![Encrypted file garbled](screenshot-garbled.png)
![Decryption success](screenshot-decrypt.png)
