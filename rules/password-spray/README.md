Document password spray rule: logic, thresholds, false positives:
# Password spray detection
- **Status:** Planned (not yet tested in lab)
- **Threat:** An attacker tries a few common passwords across many accounts to avoid lockouts.
- **MITRE ATT&CK:** T1110.003 (Password Spraying), Credential Access
- **Data source:** SigninLogs (ResultType, IPAddress, UserPrincipalName)
- **Logic:** Count failed sign-ins per IP in 15-minute windows. Alert when 10 or more distinct accounts and 20 or more failures occur.
- **Threshold reasoning:** To be completed after testing.
- **Expected false positives:** Corporate NAT, misconfigured applications, shared service accounts.
- **Tuning:** None yet.
- **Test:** Not yet tested.
- **Limitations:** Slow spraying below these thresholds will not be detected.
