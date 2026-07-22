# SSH Commands

## Connect to a Remote Machine

```bash
ssh username@IP
```

Example:

```bash
ssh kali@192.168.1.10
```

---

## Connect Using a Different Port

```bash
ssh -p PORT username@IP
```

Example:

```bash
ssh -p 2222 kali@192.168.1.10
```

---

## Run a Single Command Remotely

```bash
ssh username@IP "command"
```

Example:

```bash
ssh kali@192.168.1.10 "ls -la"
```

The command runs on the remote machine and returns the output.

---

## Generate SSH Key Pair

```bash
ssh-keygen
```

Creates:

- Private Key (`id_rsa`)
- Public Key (`id_rsa.pub`)

---

## Copy Public Key to Remote Server

```bash
ssh-copy-id username@IP
```

Example:

```bash
ssh-copy-id kali@192.168.1.10
```

Used to enable passwordless login.

---

## Login Using a Private Key

```bash
ssh -i private_key username@IP
```

Example:

```bash
ssh -i id_rsa kali@192.168.1.10
```

---

## Check SSH Version

```bash
ssh -V
```

Displays the installed SSH version.

---

## Exit SSH Session

```bash
exit
```

or

```bash
logout
```

or press:

```text
Ctrl + D
```

---

# Quick Revision

| Command | Purpose |
|---------|---------|
| `ssh username@IP` | Connect to remote machine |
| `ssh -p PORT username@IP` | Connect using custom port |
| `ssh username@IP "command"` | Execute one remote command |
| `ssh-keygen` | Generate SSH key pair |
| `ssh-copy-id username@IP` | Copy public key to server |
| `ssh -i key username@IP` | Login using private key |
| `ssh -V` | Show SSH version |
| `exit` | Disconnect from SSH session |
