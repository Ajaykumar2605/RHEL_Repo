# 📌 Linux YUM/DNF Repository Configuration – Complete Guide (RHEL / CentOS 8/9)

This repository provides complete documentation and configuration examples for all types of Linux YUM/DNF repositories used in enterprise environments.

---

## 🔥 What this guide includes
| Repository Type | Status |
|------------------|--------|
| DVD Repository | ✔ |
| Local Directory Repository | ✔ |
| HTTP Repository | ✔ |
| FTP Repository | ✔ |
| NFS Repository | ✔ |
| Online Repositories (BaseOS / AppStream / EPEL) | ✔ |

---

## 🧾 Why this repository is useful
- Helps configure repositories in **offline or secure datacenter environments**
- Works with **RHEL 8/9, Rocky Linux, AlmaLinux, CentOS Stream**
- Useful for **SysAdmins, DevOps, Linux beginners & corporates**
- Contains **step-by-step commands, repo files, firewall rules, and troubleshooting**

---

## 📂 Suggested Folder Structure
```
├── DVD_Repo/
│   └── dvd.repo
├── Local_Repo/
│   └── local.repo
├── HTTP_Repo/
│   └── http.repo
├── FTP_Repo/
│   └── ftp.repo
├── NFS_Repo/
│   └── nfs.repo
└── Online_Repo/
    └── epel.repo
```

---

## 🚀 Quick Summary of BaseURL Formats
| Repository Type | BaseURL Format | Example |
|------------------|----------------|---------|
| DVD | `file:///dvd` | RHEL ISO / DVD |
| Local Repo | `file:///repo` | Local package storage |
| HTTP Repo | `http://server/repo` | Apache hosted |
| FTP Repo | `ftp://server/pub/repo` | VSFTPD hosted |
| NFS Repo | `file:///mnt/nfsrepo` | NFS shared location |
| Online Repo | `https://` | EPEL / BaseOS / AppStream |

---

## ⚙ Validation Commands
```bash
dnf clean all
dnf repolist
dnf makecache
dnf search httpd
```

---

## ❗ Troubleshooting Table
| Issue | Solution |
|-------|----------|
| Repo not showing in list | Check `.repo` file syntax and `enabled=1` |
| Packages unavailable | Run `createrepo /path/to/repo` again |
| HTTP/FTP access blocked | Allow firewall: `firewall-cmd --add-service=http/ftp` |
| DVD not mounting | `mount -o loop /root/rhel.iso /dvd` |
| Metadata expired | `rm -rf /var/cache/dnf/* && dnf makecache` |

---

## 🏆 Maintainer
👤 **AJAY KUMAR M**  
💬 Pull Requests and Issues are most welcome!

### ✔ Final Note
This repository aims to make **Linux repository configuration simple, standardized, and production-ready** for any environment.
