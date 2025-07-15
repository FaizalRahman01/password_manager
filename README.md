AES File Encryptor & Decryptor
A Python-based command-line tool to securely encrypt and decrypt files or folders using AES-256 (CBC Mode) with a password-derived key.

Features
🔒 AES-256 Encryption (CBC Mode)

🗂️ Encrypts/Decrypts single files or entire folders recursively

🔑 SHA-256 based key derivation from user-defined password

📁 Automatically deletes original files after encryption or decryption

✅ Padding/Unpadding handled for block cipher compatibility

💻 Built using Python 3 and PyCryptodome

Requirements
Python 3.x

PyCryptodome

pip install pycryptodome  

file_to_encrypt = r"F:\Music"  # Target file or folder  
password = "YourStrongPassword"  
process_path(file_to_encrypt)  # Will encrypt files and delete originals  

file_to_decrypt = r"F:\Music"  # Target encrypted file or folder  
password = "YourStrongPassword"  
process_path(file_to_decrypt)  # Will decrypt files and delete encrypted versions  

How it Works
Derives AES key from password using SHA-256 hash

Encrypts using AES in CBC mode with a random IV

Appends .encrypted extension to encrypted files

Original files are removed after encryption/decryption for security

Disclaimer
⚠️ Use this tool responsibly. Encrypted files cannot be recovered without the correct password.
