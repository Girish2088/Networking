# Telnet

## Purpose

Telnet is a simple protocol used to create a **remote TCP connection** with another machine.

It lets you manually connect to any TCP service and communicate by typing commands.

---

## Default Port

```text
23
```

---

## How it Works

```text
Your PC
    │
    │ TCP Connection
    ▼
Remote Server
```

Once connected, you can type commands directly to the service.

---

## Common Uses

- Remote terminal (old systems)
- Test whether a TCP port is open
- Banner Grabbing
- Learn how protocols work
- CTFs
- TryHackMe
- Hack The Box

---

## Is Telnet Secure?

❌ No.

Everything is sent in plain text.

Anyone sniffing the network can read:

- Username
- Password
- Commands

Because of this, Telnet has almost completely been replaced by SSH.

---

## Example

Connect to a web server.

```bash
telnet example.com 80
```

Then type:

```http
GET / HTTP/1.1
Host: example.com

```

The server will return the HTTP response.

---

## Interview Points

- Application Layer protocol.
- Uses TCP.
- Default Port 23.
- Not encrypted.
- Replaced by SSH.

---

## Common Questions

### Q: Why is Telnet insecure?

Because all communication is plain text.

---

### Q: Which protocol replaced Telnet?

SSH.

---

## Memory Hook

```text
Telnet = Manual TCP Connection
```
