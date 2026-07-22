# FTP (File Transfer Protocol)

## Purpose

FTP is used to upload and download files between a client and a server.

---

## Default Port

```text
21
```

---

## Transport Protocol

```
TCP
```

---

## How it Works

```text
Client
   ↓
Connect to FTP Server
   ↓
Login (USER / PASS)
   ↓
Upload or Download Files
```

---

## Common Uses

- Upload Website Files
- Download Files
- Share Files
- Backup Data

---

## Is FTP Secure?

❌ No.

FTP sends:

- Username
- Password
- Data

in plain text.

---

## Secure Alternatives

- FTPS (FTP + TLS)
- SFTP (SSH File Transfer Protocol)

---

## Interview Points

- Application Layer Protocol
- Uses TCP
- Default Port 21
- Used for File Transfer
- Not Encrypted

---

## Common Questions

### Q. What is FTP?

A protocol used for transferring files.

---

### Q. Which protocol does FTP use?

TCP.

---

### Q. Which port does FTP use?

21.

---

### Q. Is FTP secure?

No.

---

## Memory Hook

```text
FTP = Upload & Download Files
```
