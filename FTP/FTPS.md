# FTPS (File Transfer Protocol Secure)

## Purpose

Securely upload and download files using TLS encryption.

---

## Why FTPS?

FTP sends data in plaintext.

FTPS adds TLS encryption to protect:

- Username
- Password
- Files

---

## Default Ports

21 + TLS (Explicit FTPS)

990 (Implicit FTPS)

---

## How it Works

Client
      ↓
TLS Handshake
      ↓
Encrypted FTP Session
      ↓
FTP Server

---

## FTP vs FTPS

FTP
- Plaintext
- No encryption

FTPS
- Encrypted
- Uses TLS

---

## Memory Hook

FTP + TLS = FTPS
