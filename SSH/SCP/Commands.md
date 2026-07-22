# SCP Commands

## Upload File (Local → Remote)

```bash
scp localfile.txt username@IP:/path/
```

Example:

```bash
scp notes.txt kali@192.168.1.10:/home/kali/
```

---

## Download File (Remote → Local)

```bash
scp username@IP:/path/file.txt .
```

Example:

```bash
scp kali@192.168.1.10:/home/kali/notes.txt .
```

---

## Copy Folder

```bash
scp -r folder username@IP:/path/
```

Example:

```bash
scp -r Projects kali@192.168.1.10:/home/kali/
```

---

## Use Different Port

```bash
scp -P 2222 file.txt username@IP:/path/
```

---

## Use Private Key

```bash
scp -i id_rsa file.txt username@IP:/path/
```

---

# Quick Revision

| Command | Purpose |
|---------|---------|
| `scp file user@IP:/path/` | Upload file |
| `scp user@IP:/path/file .` | Download file |
| `scp -r folder user@IP:/path/` | Copy folder |
| `scp -P PORT file user@IP:/path/` | Custom SSH port |
| `scp -i key file user@IP:/path/` | Use private key |
