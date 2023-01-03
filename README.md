# Web-Browser-Based-AES-GCM-File-Encryption-Decryption
Use your Web Browser to encrypt or decrypt any file with AES in Galois/Counter Mode.

## Privacy
This project features a so called self contained web page. You can run this web page offline on your system. This web page does not require any network connection. Your files and keys do not leave the web browser during the process of encryption or decryption. You can verify this by viewing the source code of this page. You can also check the network traffic while encrypting/decrypting a dummy test file.

## Cryptography
All used cryptography is implemented using the Web Browser's built in Web Crypto API. Files are encrypted using AES-GCM 256-bit symmetric encryption. The encryption key is derived from a provided password and a random salt using the PBKDF2 derivation method with 1,000,000 iterations along with SHA256 hashing.

The security depends essentially on the strength of the used password. Although the encryption uses AES-GCM with a 256-bit key, the entropy need not be 256-bit. The stronger the password, the stronger the key. If we use an alphabet with the characters [a-z][A-Z][0-9][!"§$%&/()=], we have 72 different characters to choose from. Therefore, we need at least a password consisting of 42 randomly choosen characters out of this alphabet to generate a key with 256-bit entropy. The less strong and complex your password is, the less secure your encryption will be.

## Security
You shall always check the integrity of this web page. The expected hash of the html file containing this page is posted at the project's github page. Download the plain html file and calculate the SHA256 hash. Verify that the hash of the downloaded html file matches the expected hash from the project's github site.

### Hash:
SHA256: 450a38222791f78648a0a150157ac11ef87af47e2c3a81140737a5545e35e89f
SHA1: 3dc8ff54b8edc26dd684b2e4ad256cf41fd39757
