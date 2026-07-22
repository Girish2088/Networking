# Email Protocols

## What are Email Protocols?

Email protocols are rules that allow emails to be sent, received, and synchronized between users and mail servers.

Different protocols perform different tasks.

---

# Email Journey

```text
Alice writes an email
        │
        ▼
SMTP / SMTPS
        │
        ▼
Mail Server
        │
        ├──────────────┐
        │              │
        ▼              ▼
POP3 / POP3S      IMAP / IMAPS
        │              │
        ▼              ▼
Bob reads the email
```

---

# 1. SMTP (Simple Mail Transfer Protocol)

## Purpose

SMTP is used to **send emails**.

It sends emails:

- Client → Mail Server
- Mail Server → Mail Server

SMTP **does not** read emails.

---

## Default Ports

SMTP

25

SMTPS

465

SMTP Submission (STARTTLS)

587

---

## Secure Version

SMTPS uses **TLS encryption**.

It protects:

- Username
- Password
- Email contents

---

## Memory Hook

```
SMTP

↓

Send Mail
```

---

# 2. POP3 (Post Office Protocol v3)

## Purpose

POP3 is used to **download emails** from the mail server.

Usually, after downloading, the email is removed from the server.

Best for:

- Single device

---

## Default Ports

POP3

110

POP3S

995

---

## Secure Version

POP3S uses TLS encryption.

---

## Memory Hook

```
POP3

↓

Download Mail
```

---

# 3. IMAP (Internet Message Access Protocol)

## Purpose

IMAP synchronizes emails between the mail server and multiple devices.

Emails remain stored on the server.

Best for:

- Mobile
- Laptop
- Tablet

Everything stays synchronized.

---

## Default Ports

IMAP

143

IMAPS

993

---

## Secure Version

IMAPS uses TLS encryption.

---

## Memory Hook

```
IMAP

↓

Sync Mail
```

---

# POP3 vs IMAP

| POP3 | IMAP |
|------|------|
| Downloads email | Synchronizes email |
| Usually removes email from server | Keeps email on server |
| Best for one device | Best for multiple devices |
| Faster | More flexible |

---

# SMTP vs POP3 vs IMAP

| Protocol | Purpose |
|----------|---------|
| SMTP | Send Email |
| POP3 | Download Email |
| IMAP | Synchronize Email |

---

# Secure Versions

| Protocol | Secure Version |
|----------|----------------|
| SMTP | SMTPS |
| POP3 | POP3S |
| IMAP | IMAPS |

All secure versions use **TLS encryption**.

---

# Can we see them in Wireshark?

### SMTP / POP3 / IMAP

✅ Yes

Without encryption, you may see:

- Username
- Password
- Email headers
- Email body

---

### SMTPS / POP3S / IMAPS

Only visible:

- TCP
- TLS Handshake

Email data is encrypted.

---

# Interview Questions

### What protocol sends emails?

SMTP

---

### Which protocols receive emails?

POP3

IMAP

---

### Difference between POP3 and IMAP?

POP3 downloads emails.

IMAP synchronizes emails.

---

### Why use SMTPS instead of SMTP?

SMTPS encrypts the communication using TLS.

---

### Which protocol is best for multiple devices?

IMAP

---

# Easy Story

```
Alice writes an email
        │
        ▼
SMTP sends it
        │
        ▼
Mail Server stores it
        │
        ├──────────────┐
        │              │
        ▼              ▼
POP3          IMAP
Download      Synchronize
        │              │
        ▼              ▼
Bob reads the email
```

---

# One-Line Revision

```
SMTP  → Send Email

SMTPS → Send Email Securely

POP3  → Download Email

POP3S → Download Email Securely

IMAP  → Synchronize Email

IMAPS → Synchronize Email Securely
```
