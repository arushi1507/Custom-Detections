
Description

This rule detects potential Pass-the-Hash attacks by monitoring Windows logon events that exhibit suspicious authentication patterns, such as NTLMSSP logons with a key length of zero or Seclogon processes using the Negotiate authentication package. These behaviors may indicate an attacker using stolen NTLM hashes to authenticate across multiple systems without knowing the actual password. The detection focuses on accounts making logons to multiple distinct destinations within a short time frame, which is common in lateral movement scenarios. Recommended Triage Actions:
- Review the source account and system initiating the suspicious logons.
- Check for recent privilege escalation or credential dumping activity on the source host.
- Validate whether the logons are legitimate administrative actions or unauthorized access.
- Isolate affected systems if malicious activity is confirmed.
- Reset credentials for compromised accounts.
Category: LateralMovement Tag: SplunkMigrated
Scheduling type
Scheduled
Incident correlation
Enabled

MITRE ATT&CK

LateralMovement
T1550: Use Alternate Authentication Material
