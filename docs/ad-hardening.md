# Active Directory hardening baseline

Status: in progress. Items are ticked only when applied and verified in the lab.

## Priority 1: protocol and credential hardening

- [ ] SMB signing required (GPO)
- [ ] LDAP signing required and channel binding enabled
- [ ] LLMNR disabled (GPO)
- [ ] NetBIOS over TCP/IP disabled
- [ ] LAPS deployed for the Endpoints OU

## Priority 2: privileged access and Kerberos

- [ ] Protected Users group in use for privileged accounts
- [ ] Delegation disabled on privileged accounts
- [ ] RC4 and DES disabled, AES enforced
- [ ] KRBTGT password rotated twice

## Priority 3: auditing

- [ ] Advanced Audit Policy GPO
- [ ] Key event IDs monitored
- [ ] Sysmon on Windows VMs

## Doc template for each item

For every item above, add a short section with:

- **Setting and GPO path**
- **Why it matters** (the attack it reduces)
- **Before and after evidence** (command output or screenshot)
- **Rollback**

Tick the box only after the evidence is added.
