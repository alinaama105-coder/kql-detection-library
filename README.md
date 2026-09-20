KQL Detection Library

KQL queries from my Microsoft Sentinel lab and security monitoring practice.

Rather than keeping long notes here, the query files contain the working examples I use for SSH authentication and investigation.

---

Queries

- `queries/failed-ssh.kql` — failed SSH authentication
- `queries/successful-ssh.kql` — successful SSH authentication
- `queries/failed-ssh-threshold.kql` — repeated failures over a five-minute window
- `queries/source-ip-extraction.kql` — extract source IPs from sshd messages
- `queries/failed-auth-by-source.kql` — count failures by source IP
- `queries/recent-ssh-activity.kql` — recent SSH activity
- `queries/authentication-summary.kql` — summarise authentication events
- `queries/suspicious-ip-investigation.kql` — search for activity from an IP under investigation

---

What I Used This For

In my Sentinel lab I used KQL to review failed and successful SSH authentication, extract source IP addresses and build detection logic around repeated failures.

I also practised investigating a successful login following repeated failures and created a watchlist called `Malicious SSH IPs`.

My basic workflow is:

Logs → KQL → Detection → Alert → Incident → Investigation

---

Current Focus

I am continuing to work on authentication analysis, Sentinel analytics rules, watchlist correlation, identity monitoring and alert enrichment.

Progress still ongoing.
