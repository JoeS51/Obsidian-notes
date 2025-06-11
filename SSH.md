## 🛠 SSH Key Setup

1. ****Generate SSH key:****

   ```bash

   ssh-keygen -t rsa -b 2048 -f ~/.ssh/id_rsa

   ```

   → This creates:

   - `~/.ssh/id_rsa` → your private key (keep it safe)

   - `~/.ssh/id_rsa.pub` → your public key (share with server admin)
---
## 🌐 SSH Into the Server

- Without config:

  ```bash

  ssh -i ~/.ssh/id_rsa genzart@73.114.169.125 -p 8145

  ```
- With `~/.ssh/config` setup:

  ```

  Host genzart-server

    HostName 73.114.169.125

    User genzart

    Port 8145

    IdentityFile ~/.ssh/id_rsa

  ```

  → Then connect using:

  ```bash

  ssh genzart-server

  ```

  

---

  

## 🔐 Password Notes

  

- ****SSH key password**** → the passphrase you set for your private key.

- ****Server password (if asked)**** → `esteghlal1234`.

  

---

  

## 🖥 Using tmux

  

Once logged in:

```bash

tmux attach

```

  

- `Ctrl + Space` → main command prefix.

  - `Ctrl + Space` → then `c` → new window.

  - `Ctrl + Space` → then `0` or `1` → switch windows.

  - `Ctrl + Space` → then `-` → split horizontal.

  

⚠ ****Be careful not to close or kill existing tmux sessions**** — they might be running important processes.

  

---

  

## 🏓 Checking Server Connectivity

  

- ****Ping (general machine check):****

  ```bash

  ping 73.114.169.125

  ```

  ⚠ If you get:

  ```

  Request timeout for icmp_seq ...

  ```

  it might just mean ping is blocked — not that the server is down.

  

- ****Check if SSH port is open:****

  ```bash

  nc -zv 73.114.169.125 8145

  ```

  or

  ```bash

  telnet 73.114.169.125 8145

  ```

  

---

  

## 📦 Summary

  

✅ SSH keys → avoid typing passwords.  

✅ tmux → keep processes running even after disconnect.  

✅ Use SSH config → simplify commands.  

✅ Test port, not just ping, to check server status.