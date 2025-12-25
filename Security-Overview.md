# Security Overview

## Encryption Method
- The system uses **AES (Advanced Encryption Standard)** for encrypting all uploaded files.
- Each file gets a **unique 16-byte encryption key**.
- AES ensures data confidentiality and integrity.

## Key Management
- Encryption keys are **stored separately** in the `keys/` folder.
- Only authorized personnel with access to the keys can decrypt files.
- Keys are generated using a **secure random generator**.

## File Handling Security
- Files are **encrypted before being saved** on the server.
- Uploaded files are stored in the `uploads/` folder in encrypted form.
- Decrypted data is never stored permanently on the server.

## Recommendations (for improvement)
- Implement AES in **CBC mode with IV** for better security.
- Add user authentication to control who can upload/download files.
- Secure the communication channel using **HTTPS**.

