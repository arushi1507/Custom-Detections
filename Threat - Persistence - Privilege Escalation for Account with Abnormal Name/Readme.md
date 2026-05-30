Description
This detection identifies instances where a user account with an unusual or abnormal naming convention is added to an administrative role in Azure Active Directory. Such activity may indicate privilege escalation by a potentially compromised or malicious account, especially if the account name does not match expected organizational patterns. The rule filters out known exceptions and focuses on successful role assignment events that could grant elevated privileges. This behavior is often associated with persistence tactics, where attackers maintain long-term access by creating or modifying privileged accounts.

Recommended Triage Actions:
- Review the affected account’s creation history and naming pattern for legitimacy.
- Verify whether the role assignment was authorized and aligns with business needs.
- Check for recent login activity and unusual sign-in locations for the account.
- Investigate any related changes in Azure AD logs, such as password resets or MFA status changes.
- Remove unauthorized role assignments and disable suspicious accounts if necessary.

Category: Persistence Tag: SplunkMigrated
Scheduling type
Scheduled
Incident correlation
Enabled

MITRE ATT&CK

Persistence
T1136: Create Account
PrivilegeEscalation

