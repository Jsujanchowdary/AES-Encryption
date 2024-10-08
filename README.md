# OpenSSL AES-256-CBC Encryption/Decryption Example

This repository demonstrates how to encrypt and decrypt text files using the OpenSSL command line tool with the AES-256-CBC algorithm.

## Prerequisites

Make sure OpenSSL is installed on your system. You can verify its installation by running the following command in your terminal:

```bash
openssl version
```

## Encryption Process

To encrypt a text file using AES-256-CBC encryption, use the following command:

```bash
openssl enc -aes-256-cbc -e -in <input_file> -out <output_encrypted_file>
```

- `<input_file>`: Path to the original text file that you want to encrypt.
- `<output_encrypted_file>`: Path where the encrypted file will be saved.

### Example:

```bash
openssl enc -aes-256-cbc -e -in text.txt -out encryptedtextfile.text
```

You will be prompted to provide a password. This password will be required for decryption later.

## Decryption Process

To decrypt the encrypted file, use the following command:

```bash
openssl enc -aes-256-cbc -d -in <encrypted_file> -out <output_decrypted_file>
```

- `<encrypted_file>`: Path to the file that was encrypted.
- `<output_decrypted_file>`: Path where the decrypted file will be saved.

### Example:

```bash
openssl enc -aes-256-cbc -d -in encryptedtextfile.text -out decryptedtextfile.text
```

You will be prompted to enter the password used during the encryption process.

## Warnings

When running the above commands, you may encounter a warning regarding the use of deprecated key derivation methods. This is a known issue with some versions of OpenSSL and does not impact the encryption and decryption processes in this context.

## Observations

1. **Encryption**: The encryption was successful using the `openssl enc -aes-256-cbc -e` command. The encrypted output was saved as `encryptedtextfile.text`. However, a warning was issued about deprecated key derivation methods.
   
2. **Decryption**: The decryption was successfully performed using the `openssl enc -aes-256-cbc -d` command. The decrypted file was saved as `decryptedtextfile.text`, with the same warning about deprecated key derivation methods.
