# Email Protocol Commands

These commands can be tested using **Telnet** or **Netcat**.

---

# SMTP Commands

## Connect

```bash
telnet mail.server.com 25
```

or

```bash
nc mail.server.com 25
```

### Start Session

```text
HELO hostname
```

or

```text
EHLO hostname
```

---

### Specify Sender

```text
MAIL FROM:<sender@example.com>
```

---

### Specify Recipient

```text
RCPT TO:<receiver@example.com>
```

---

### Write Email

```text
DATA
```

Finish the message with:

```text
.
```

---

### Quit

```text
QUIT
```

---

# POP3 Commands

## Connect

```bash
telnet mail.server.com 110
```

---

### Login

```text
USER username

PASS password
```

---

### List Emails

```text
LIST
```

---

### Read Email

```text
RETR 1
```

---

### Delete Email

```text
DELE 1
```

---

### Quit

```text
QUIT
```

---

# IMAP Commands

## Connect

```bash
telnet mail.server.com 143
```

---

### Login

```text
LOGIN username password
```

---

### List Mailboxes

```text
LIST "" *
```

---

### Open Inbox

```text
SELECT INBOX
```

---

### Read Email

```text
FETCH 1 BODY[]
```

---

### Logout

```text
LOGOUT
```

---

# Quick Revision

## SMTP

| Command | Purpose |
|----------|---------|
| EHLO | Start session |
| MAIL FROM | Sender |
| RCPT TO | Recipient |
| DATA | Write email |
| QUIT | Exit |

---

## POP3

| Command | Purpose |
|----------|---------|
| USER | Username |
| PASS | Password |
| LIST | List emails |
| RETR | Read email |
| DELE | Delete email |
| QUIT | Exit |

---

## IMAP

| Command | Purpose |
|----------|---------|
| LOGIN | Login |
| LIST | List mailboxes |
| SELECT | Open mailbox |
| FETCH | Read email |
| LOGOUT | Exit |
