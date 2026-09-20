# 🔐 Week 1 — Password Security & Hashing Lab

**Internship Task | Muhammad Haseeb | IMSciences Peshawar**

---

## 📋 Task Overview

| Field | Details |
|---|---|
| Platform | TryHackMe — Crack the Hash Room |
| Difficulty | Intermediate |
| Duration | 4–5 Days |
| Status | ✅ Completed |

---

## 🎯 Objective

Study password hashing, salting, and common cracking techniques
using an authorized CTF-style lab. Document tools, methodology,
and produce secure password storage recommendations for a client.

---

## 📚 Concepts Studied

- **Plaintext Storage** — most dangerous, no protection
- **Encryption** — reversible, never use for passwords
- **Hashing** — one-way, irreversible (MD5, SHA-1, SHA-256)
- **Salting** — unique random value per user, defeats rainbow tables
- **Key Stretching** — thousands of hash rounds (bcrypt, Argon2)
- **Slow Hashing** — deliberately slow algorithms for passwords
- **Memory-Hard Hashing** — requires RAM, defeats GPU attacks (Argon2id)

---

## 🛠️ Tools Used

| Tool | Purpose |
|---|---|
| TryHackMe | Authorized lab environment |
| `hashid` | Hash type identification (run first always) |
| `hashid -m` | Get Hashcat mode number |
| CrackStation | Primary online hash cracker |
| Hashes.com | Secondary cracker for bcrypt/SHA-512crypt |
| Hashcat | Dictionary attacks + identification |

### Commands Used
```bash
# Identify hash type
hashid '<hash_value>'
hashid -m '<hash_value>'

# Crack with dictionary
hashcat -m <mode> '<hash>' /usr/share/wordlists/rockyou.txt

# Mode numbers
# 0    = MD5       | 100  = SHA-1
# 1400 = SHA-256   | 900  = MD4
# 1000 = NTLM      | 1800 = SHA-512crypt
# 3200 = bcrypt
```

---

## 🚩 Lab Results

### Beginner Level

| # | Hash Type | Password | Status |
|---|---|---|---|
| 1 | MD5 | easy | ✅ Cracked |
| 2 | SHA-1 | password123 | ✅ Cracked |
| 3 | SHA-256 | letmein | ✅ Cracked |
| 4 | bcrypt | bleh | ✅ Cracked |
| 5 | MD4 | Eternity22 | ✅ Cracked |

### Intermediate Level

| # | Hash Type | Password | Status |
|---|---|---|---|
| 1 | SHA-256 | paule | ✅ Cracked |
| 2 | NTLM | n63umy8lkf4i | ✅ Cracked |
| 3 | SHA-512crypt | waka99 | ✅ Cracked |
| 4 | SHA-1 | 481616481616 | ✅ Cracked |

**Total: 9/9 cracked (100% success rate)**

---

## 🧠 Key Learnings

- MD5 and SHA-1 crack in **seconds** — never use for passwords
- Without salting, rainbow tables crack everything instantly
- bcrypt cracked here only because password was weak (4 chars)
- `hashid` must always be run **before** any cracking attempt
- Strong algorithm + unique salt + strong password = complete defence

---

## 📄 Deliverables

- ✅ Full Lab Report PDF (see `lab-writeup.pdf`)
- ✅ SafeX Client Recommendations (submitted to Group Leader)
- ✅ Submitted before Friday deadline

---

## 📚 References

- [TryHackMe — Crack the Hash](https://tryhackme.com/room/crackthehash)
- [OWASP Password Storage Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Password_Storage_Cheat_Sheet.html)
- [HaveIBeenPwned API](https://haveibeenpwned.com/API/v3)
- [Hashcat Wiki](https://hashcat.net/wiki/)
