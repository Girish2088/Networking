# Network Services

Network Services help devices communicate across different networks and provide essential networking functions such as routing packets, translating IP addresses, tracing packet paths, and retrieving domain information.

---

# Routing

## Purpose

Routing is the process of selecting the best path for a packet to travel from the source network to the destination network.

---

## How It Works

```text
Laptop
   │
Home Router
   │
ISP Router
   │
Internet
   │
Web Server
```

Each router checks its **Routing Table** and forwards the packet to the next best hop.

---

## Key Points

- Works at **Layer 3 (Network Layer)**.
- Uses **IP Addresses**.
- Performed by **Routers**.
- Uses **Routing Tables** to determine the best path.

---

## Interview Answer

> Routing is the process of selecting the best path for packets to travel from the source network to the destination network.

---

# NAT (Network Address Translation)

## Purpose

NAT translates **Private IP Addresses** into **Public IP Addresses**, allowing devices on a private network to communicate with the Internet.

---

## How It Works

```text
Laptop

192.168.1.10
      │
      ▼
Router (NAT)
      │
      ▼
49.xx.xx.xx
      │
      ▼
Internet
```

The Internet only sees the **Public IP Address**.

---

## Why NAT?

- Allows multiple devices to share one Public IP.
- Conserves Public IPv4 addresses.
- Hides internal network addresses.

---

## Key Points

- Works at **Layer 3 (Network Layer)**.
- Converts **Private IP ↔ Public IP**.
- Performed by the **Router**.

---

## Interview Answer

> NAT translates private IP addresses into public IP addresses so private devices can access the Internet while conserving public IPv4 addresses.

---

# Traceroute

## Purpose

Traceroute shows every router (**hop**) a packet passes through before reaching its destination.

---

## Example

```text
My Laptop
      ↓
Home Router
      ↓
ISP Router
      ↓
Regional Router
      ↓
Destination Server
```

---

## Commands

### Linux

```bash
traceroute google.com
```

### Windows

```cmd
tracert google.com
```

---

## Uses

- Troubleshoot network problems.
- Find where packet loss occurs.
- Measure network path.

---

## Key Points

- Uses **TTL (Time To Live)**.
- Shows every **Hop**.
- Common troubleshooting tool.

---

## Interview Answer

> Traceroute is a network diagnostic tool that displays the path packets take to reach a destination.

---

# WHOIS

## Purpose

WHOIS retrieves registration information about a domain name.

---

## Command

```bash
whois google.com
```

---

## Information It Can Show

- Domain Owner (if public)
- Registrar
- Registration Date
- Expiry Date
- Name Servers

---

## Uses

- Domain investigation
- Security research
- Ownership verification

---

## Key Points

- WHOIS is **not DNS**.
- WHOIS does **not** resolve IP addresses.
- WHOIS provides **domain registration information**.

---

## Interview Answer

> WHOIS is a protocol used to retrieve registration information about a domain name.

---

# Simple Flow

```text
Need a Website
      ↓
DNS
(Get Server IP)
      ↓
Routing
(Choose Best Path)
      ↓
NAT
(Convert Private IP → Public IP)
      ↓
Internet
      ↓
Website Loads
```

---

# One-Line Revision

```text
Routing    → Chooses the Best Path

NAT        → Private IP ↔ Public IP

Traceroute → Shows Every Hop

WHOIS      → Domain Registration Information
```

---

# Memory Hooks

```text
Routing    = Packet Navigation System

NAT        = Internet Translator

Traceroute = GPS of a Packet

WHOIS      = Domain Information
```
