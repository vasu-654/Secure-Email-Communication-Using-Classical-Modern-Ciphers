**🔍 Problem Statement**


With increasing concerns around email privacy, especially in application accounts used for automated communication (e.g., alert systems, reporting bots, transactional services), there is a strong need to restrict visibility of email content even if the account itself is compromised or accessed by unintended users.

This project addresses that problem by allowing you to encrypt email content using classic and modern cryptographic algorithms before sending, ensuring that only the intended recipient with the right key can decrypt and read the message.


**📌 Project Overview**

This is a Python-based terminal application that allows a user to:

Send encrypted emails using various encryption techniques.
Read and decrypt received emails securely.
Use classic ciphers like Caesar, Monoalphabetic, Playfair, and Polyalphabetic.
Use modern cryptography like DES and AES for stronger security.
It is designed specifically for application accounts, where:
Communication is often automated.
Human-readable protection is necessary even if the account credentials are exposed.


**🔧 Features**

✅ Caesar Cipher
✅ Monoalphabetic Cipher
✅ Playfair Cipher
✅ Polyalphabetic Cipher (Vigenère-style)
✅ DES Encryption
✅ AES Encryption (EAX mode for integrity + confidentiality)
📤 Send encrypted content via SMTP
📥 Read and decrypt emails via IMAP



**⚙️ Technologies Used**

Python 3.x
smtplib – Sending emails via SMTP
imaplib – Reading emails via IMAP
pycryptodome – For DES and AES encryption
email – MIME email formatting and parsing


**🔐 Security Considerations**

⚠️ This system is designed primarily for application-specific accounts, such as Gmail App Passwords.
Do NOT use your main email credentials directly.

Use App Passwords if using Gmail or similar providers with 2FA enabled.
Store credentials in a .env file or encrypted secrets vault if using in production.
DES is included for demonstration but is not considered secure.
AES encryption uses EAX mode for better cryptographic integrity.
Email content remains secure even if email credentials are leaked, unless the encryption key is also compromised.



**🚀 Getting Started**

**📥 Prerequisites**
pip install pycryptodome


**🧪 Run the Program**

python email_encryption.py


**🛠️ How to Use**

Choose whether you want to:
Send an encrypted email
Read and decrypt an incoming email
Select your preferred encryption algorithm:
Choose from Caesar, Monoalphabetic, Playfair, Polyalphabetic, DES, or AES
Enter your message and a key (if required).
The email is encrypted and sent to the recipient.
The recipient can decrypt the email content using the same algorithm and key.


**🧠 Example Use Case**

Imagine you're using an automated application account to send system reports or logs. These logs may contain sensitive data (e.g., server IPs, user activities). Encrypting the content ensures that even if someone accesses the email inbox, the actual message content remains protected unless they also have the correct key.



**📧 Email Configuration**

⚠️ Replace placeholders with your actual email and app password in the code:

email = "your_application_email@gmail.com"

password = "your_app_password_here"

Avoid using your primary email or personal password. Use application-specific passwords for improved safety.



**🧩 Future Improvements**

GUI version using PyQt or Tkinter
Integration with encrypted storage (key vault)
QR-code-based key sharing
Support for asymmetric encryption (RSA, ECC)
