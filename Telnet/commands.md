# Telnet Commands

## Connect to a Service

```bash
telnet IP PORT
```

Example:

```bash
telnet 192.168.1.10 80
```

---

## Test HTTP

```bash
telnet example.com 80
```

```http
GET / HTTP/1.1
Host: example.com

```

---

## Test SMTP

```bash
telnet mail.example.com 25
```

---

## Test POP3

```bash
telnet mail.example.com 110
```

---

## Test IMAP

```bash
telnet mail.example.com 143
```

---

## Exit

Press:

```
Ctrl + ]
```

Then type:

```text
quit
```
