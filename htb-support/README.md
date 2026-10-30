# Support – HackTheBox (Easy)

**Platform**: HackTheBox (retired machine)
**OS**: Windows Server (Active Directory, Domain Controller)
**Difficulty**: Easy
**Date**: October 2026

## Summary

First Active Directory machine I completed. A non-default SMB share exposes
a custom .NET tool; decompiling it reveals an obfuscated service account
password, which leads to an LDAP-stored credential, a WinRM foothold, and
full domain compromise via a `GenericAll` → RBCD attack path identified
with BloodHound.

## Full write-up

[writeup.md](writeup.md)

## Vulnerabilities covered

Hardcoded/obfuscated credential in a binary, secret stored in a free-text
LDAP attribute, excessive AD permission (`GenericAll`), RBCD abuse.

⚠️ Educational content only, carried out on a retired training machine.