# SFTP Commands

## Connect to Server

```bash
sftp username@IP
```

Example:

```bash
sftp kali@192.168.1.10
```

---

## Connect Using Private Key

```bash
sftp -i id_rsa username@IP
```

---

## List Remote Files

```bash
ls
```

---

## Show Current Remote Directory

```bash
pwd
```

---

## Change Remote Directory

```bash
cd folder
```

---

## Show Current Local Directory

```bash
lpwd
```

---

## Change Local Directory

```bash
lcd folder
```

---

## Download File

```bash
get filename
```

Example:

```bash
get notes.txt
```

---

## Upload File

```bash
put filename
```

Example:

```bash
put notes.txt
```

---

## Create Remote Directory

```bash
mkdir folder
```

---

## Remove Remote File

```bash
rm filename
```

---

## Rename Remote File

```bash
rename old.txt new.txt
```

---

## Exit

```bash
exit
```

or

```bash
bye
```

---

# Quick Revision

| Command | Purpose |
|---------|---------|
| `sftp user@IP` | Connect |
| `ls` | List remote files |
| `pwd` | Show remote directory |
| `cd` | Change remote directory |
| `lpwd` | Show local directory |
| `lcd` | Change local directory |
| `get file` | Download file |
| `put file` | Upload file |
| `mkdir` | Create directory |
| `rm file` | Delete file |
| `rename old new` | Rename file |
| `exit` | Disconnect |
