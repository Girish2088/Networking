# 🌐 Networking Protocols

This document covers the basic networking protocols used for communication over a network.

---

# DNS (Domain Name System)

## Purpose

Converts a **Domain Name** into an **IP Address**.

Without DNS, we would have to remember IP addresses instead of website names.

---

## How it Works

```text
User enters:
google.com
      ↓
DNS Server
      ↓
Returns IP Address
      ↓
Browser connects to the website
```

---

## Default Port

```text
53
```

- UDP → Most DNS queries
- TCP → Large responses and Zone Transfers

---

## Example

```text
google.com
      ↓
DNS
      ↓
142.250.x.x
```

---

## Interview Points

- DNS works at the **Application Layer**.
- Converts Domain Name → IP Address.
- Uses Port **53**.
- Mostly uses UDP.

---

## Common Questions

### Q: Why do we need DNS?

So users can use website names instead of remembering IP addresses.

---

### Q: Which port does DNS use?

Port **53**.

---

### Q: Does DNS use TCP or UDP?

Mostly UDP.
TCP is used for large responses and zone transfers.

---

## Useful Commands

```bash
nslookup google.com
```

```bash
dig google.com
```

---

## Memory Hook

```text
DNS = Internet Phonebook
```

---

# ICMP (Internet Control Message Protocol)

## Purpose

Used for:

- Connectivity Testing
- Error Reporting
- Network Troubleshooting

ICMP does **not** transfer website or application data.

---

## How it Works

```text
PC
 ↓
"Are you alive?"
 ↓
Server
 ↓
"Yes"
```

---

## Common Uses

- Ping
- Traceroute
- Error messages

---

## Interview Points

- ICMP works at the **Network Layer**.
- Used for diagnostics.
- Does not use ports.
- Does not use TCP or UDP.

---

## Common Questions

### Q: Which command uses ICMP?

```
ping
```

---

### Q: Does ICMP use TCP or UDP?

No.

It is its own protocol.

---

## Useful Commands

```bash
ping google.com
```

```bash
traceroute google.com
```

---

## Memory Hook

```text
ICMP = Network Health Check
```

---

# HTTP (HyperText Transfer Protocol)

## Purpose

Transfers web pages between a browser and a web server.

HTTP data is **not encrypted**.

---

## How it Works

```text
Browser
      ↓
HTTP Request
(GET / POST)
      ↓
Web Server
      ↓
HTTP Response
(HTML, CSS, JS, Images)
```

---

## Default Port

```text
80
```

---

## Common Methods

| Method | Purpose |
|---------|---------|
| GET | Retrieve data |
| POST | Send data |
| PUT | Create / Update |
| DELETE | Remove data |

---

## Example

```text
Browser
      ↓
GET /
Host: example.com
      ↓
Web Server
      ↓
Returns Web Page
```

---

## Interview Points

- HTTP works at the **Application Layer**.
- Uses TCP.
- Default Port is **80**.
- Data is sent in Plain Text.

---

## Common Questions

### Q: Is HTTP secure?

No.

HTTP sends data in plain text.

---

### Q: Which transport protocol does HTTP use?

TCP.

---

### Q: Which port does HTTP use?

Port **80**.

---

## Useful Commands

```bash
curl http://example.com
```

```bash
telnet IP 80
```

```bash
nc IP 80
```

---

## Important Notes

If the webpage is already stored in the **browser cache**, the browser may load it locally.

In that case, you may **not see HTTP packets in Wireshark**.

To generate new HTTP packets:

- Open an Incognito window.
- Disable browser cache.
- Clear browser cache.
- Visit a new website.

---

## Memory Hook

```text
HTTP = Read and Send Web Pages
```

---

# HTTPS (HyperText Transfer Protocol Secure)

## Purpose

HTTPS is **HTTP protected by TLS**.

It encrypts communication between the browser and the web server.

---

## How it Works

```text
Browser
     ↓
DNS Lookup
     ↓
TCP Three-Way Handshake
     ↓
TLS Handshake
     ↓
Encrypted HTTP Communication
```

---

## Default Port

```text
443
```

---

## TLS Provides

- Encryption
- Integrity
- Authentication

---

## HTTP vs HTTPS

| HTTP | HTTPS |
|------|--------|
| Port 80 | Port 443 |
| No Encryption | Encrypted |
| Plain Text | Secure using TLS |

---

## Example

```text
https://google.com
      ↓
TLS Handshake
      ↓
Encrypted Communication
```

---

## Interview Points

- HTTPS works at the **Application Layer**.
- Uses TCP.
- Default Port is **443**.
- Uses TLS for secure communication.

---

## Common Questions

### Q: What is the difference between HTTP and HTTPS?

HTTP sends data in plain text.

HTTPS encrypts the communication using TLS.

---

### Q: Does HTTPS replace HTTP?

No.

HTTPS is simply HTTP running over TLS.

---

### Q: Why is HTTPS more secure?

Because it provides:

- Encryption
- Integrity
- Authentication

---

## Useful Commands

```bash
curl https://example.com
```

---

## Memory Hook

```text
HTTPS = Secure Web Traffic
```

---

# Quick Revision

```text
DNS
→ Domain Name → IP Address

ICMP
→ Connectivity Testing & Error Reporting

HTTP
→ Load Web Pages

HTTPS
→ Secure HTTP using TLS
```

---

# Port Revision

```text
DNS    → 53

HTTP   → 80

HTTPS  → 443

ICMP   → No Port
```

---

# Website Journey

```text
User enters URL
        ↓
DNS resolves Domain Name
        ↓
TCP Connection
        ↓
(TLS Handshake if HTTPS)
        ↓
HTTP/HTTPS Request
        ↓
Web Server
        ↓
HTTP/HTTPS Response
        ↓
Browser Displays Website
```
