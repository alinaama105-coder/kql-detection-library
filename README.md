KQL Detection Library

KQL queries from my Microsoft Sentinel and security monitoring practice.

The queries focus on authentication activity, SSH monitoring, suspicious IP investigation and SOC-style log analysis.

---

Failed SSH Authentication

Purpose:

Identify failed SSH authentication attempts and review the source IP addresses generating them.

Used for reviewing failed SSH activity during my Sentinel lab.

See: queries/failed-ssh.kql

---

Repeated SSH Failures

Purpose:

Identify multiple failed SSH authentication attempts within a short period.

This formed the basis of a Sentinel detection rule for repeated SSH failures.

See: queries/failed-ssh-threshold.kql

---

Successful SSH Authentication

Purpose:

Review successful SSH logins.

See: queries/successful-ssh.kql

---

Source IP Extraction

Purpose:

Extract an IP address from SSH log data so authentication activity can be grouped and investigated by source.

See: queries/source-ip-extraction.kql

---

Failed Authentication by Source IP

Purpose:

Count failed SSH attempts from individual source IP addresses.

See: queries/failed-auth-by-source.kql

---

Successful Login After Failures

Repeated authentication failures followed by a successful login can require further investigation.

The analyst should review:

- Source IP
- Username
- Target host
- Number of failures
- Successful login
- Time between events
- Other activity from the same source

I used this type of sequence during my Sentinel detection and incident investigation practice.

---

Time-Based Investigation

Useful when reviewing recent activity around an alert.

See: queries/recent-ssh-activity.kql

---

Authentication Summary

Useful for identifying periods with increased SSH activity.

See: queries/authentication-summary.kql

---

Suspicious IP Investigation

Once a suspicious IP has been identified, I can search for additional activity associated with that address.

See: queries/suspicious-ip-investigation.kql

---

Watchlist Investigation

During my Sentinel practice I created a watchlist called:

Malicious SSH IPs

Watchlists can be used to compare known indicators with activity appearing in security logs.

Areas being developed further:

- Watchlist correlation
- IP matching
- Indicator enrichment
- Detection logic

---

Microsoft Entra ID

My Entra ID practice included reviewing successful and failed sign-in activity.

Investigation areas include:

- User
- Timestamp
- Authentication result
- Failure reason
- Error code
- Source IP
- Repeated failures
- Account lockout behaviour

KQL investigation of identity logs is an area I am continuing to develop.

---

Detection Development

Current workflow:

Logs
↓
KQL query
↓
Suspicious activity identified
↓
Analytics rule
↓
Alert
↓
Incident
↓
Investigation

My Sentinel lab included analytics rules for repeated failed SSH authentication and successful authentication following failures.

---

Current Focus

- Authentication analysis
- SSH monitoring
- Source IP investigation
- Detection engineering fundamentals
- Sentinel analytics rules
- Watchlist correlation
- Identity monitoring
- Alert enrichment
- Reducing unnecessary alert noise

Progress still ongoing.
