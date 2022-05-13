# Personal notes to use in a RT engagement

### 1. Start with good old Nessus/Nmap over the in-scope ranges.

### 2. Setup Mitm6, NTLMRelayX, Responder, CME in gen-relay-list mode and PCredz.

### 3. Use Aquatone or WirnessMe/EyeWitness

### 4. Look for NULL session enumeration against the DC

Use: [enum4linux-ng](https://github.com/cddmp/enum4linux-ng)

```bash
enum4linux -A DC.acme.local
```

### 5. Use kerbrute

Use: [Kerbrute](https://github.com/ropnop/kerbrute)

### 6. Look for patterns in the username. Create a wordlist of potentially valid users.

```bash
kerbrute userenum -d acme.local -o valid_users.txt potential_users.txt
```

### 7. FUZZ web services

### 8. Crack SPNs

### 9. Look for AS-REP roastable users

### 10. Look for GPP-Passwords & GPP-Autologin

### 11. Run bloodhound from a non-joined domain

```bash
runas /netonly /user:acme.local\username powershell
```
### 12. Try using [koadic](https://github.com/fymore/koadic) for a reverse shell

### 13. Run rubeus to steal tickets from machine
