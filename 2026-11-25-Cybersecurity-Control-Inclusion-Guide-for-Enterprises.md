# Cybersecurity Control Inclusion Guide for Enterprises

Created on 2026-11-25 07:20  
Published on ---

Built on the evidence in *House of Cards: Why Enterprise Cybersecurity Is Collapsing Under Speed, Complexity and Deferred Decisions*.

Large organisations are not failing because they lack tools. They are failing because the operating model (periodic assessment + ticket-based remediation + headcount-driven hiring) has been inverted by machine-speed attackers, toxic combinations, and decision latency.

This guide translates those findings into specific controls enterprises should include or harden, prioritised for Tier-0 and crown-jewel assets.

### 1. Speed Inversion Controls

**Evidence:** Average eCrime breakout time is 29 minutes (fastest observed 27 seconds). Median time to fully remediate a CISA KEV vulnerability is 43 days. Only 26% of KEV flaws are fully remediated.

**Controls to include:**

- Pre-authorised automated isolation of compromised identities and workloads. Detection must be able to trigger isolation without a meeting for defined high-severity conditions on Tier-0 systems.
- Microsegmentation with real-time enforcement and default-deny east-west for crown-jewel applications and data stores.
- Measure Mean Time to Isolate (MTTI), not only Mean Time to Detect.
- KEV-first patching with automated validation and hard SLAs (internet-facing and Tier-0 treated separately from the general vulnerability queue).

### 2. Toxic Combination and Continuous Exposure Controls

**Evidence:** Vulnerability exploitation is now the leading initial-access vector (31%). Third parties appear in 48% of breaches. Compounding risks appear in a majority of major breaches studied.

**Controls to include:**

- Continuous compound risk scoring that evaluates assets and identities against defined toxic combinations (privileged identity + unpatched KEV + weak monitoring; stale vendor credential + broad cloud permissions + no key-age alerting; missing MFA on a third-party cloud account holding sensitive data; privileged AI agent + unconstrained tool access).
- Prioritise by combination severity and blast radius rather than single CVSS scores.
- Maintain a living view of open toxic combinations on crown-jewel assets, with owners and target close dates.

### 3. Identity and Credential Lifecycle Controls

**Evidence:** Non-human identities, unretired vendor keys, and excessive privilege recur across recent incidents. Only 23% of third parties fully remediated missing MFA on cloud accounts.

**Controls to include:**

- Full inventory and governance of non-human identities, service accounts, API keys, cloud access keys, OAuth apps, and AI agents with the same rigour as human identities.
- Named owner, expiry, and last-used date on every credential. Automated revocation of credentials tied to completed projects (target: 24 hours after project end).
- Key-age alerting and forced rotation.
- Least privilege and just-in-time access for human, service, and AI-agent identities.
- Mandatory and continuously verified MFA on all third-party cloud accounts that hold company data.

### 4. Third-Party and AI Vendor Controls

**Evidence:** Entry is frequently via unretired vendor keys or compromised AI/infrastructure providers.

**Controls to include:**

- Same remediation SLAs for material vendors as for internal teams on issues that affect company data or access.
- Continuous monitoring of vendor-issued credentials (age, last use, permissions).
- Default-deny egress and tight scoping for AI vendors and inference providers.
- Contractual right to audit and immediate notification/revocation on vendor compromise.

### 5. Decision Latency and Operating Model Controls

**Evidence:** Skills gaps now outweigh headcount shortages. Deferred critical hires extend exposure windows.

**Controls to include:**

- Decision-rights SLAs with Board visibility: critical security requisitions ≤ 10 business days; risk exceptions on KEV flaws ≤ 7 days then Board-visible; emergency isolation of Tier-0 pre-authorised.
- Treat critical skill gaps (AI security, cloud identity, continuous exposure management) as operational risk items.
- Fund containment and identity controls before additional detection dashboards.

### 6. AI Agent Controls

**Evidence:** Agentic tooling and AI infrastructure providers are active attack vectors. Many organisations lack proper AI access controls.

**Controls to include:**

- Inventory every AI agent and AI vendor with data or key access.
- Least privilege, default-deny egress, full audit, short-lived scoped credentials, and a kill-switch.
- Monitoring for anomalous agent behaviour and prompt/tool abuse.

### Prioritisation Order

1. Credential lifecycle (vendor and non-human) + MFA on third-party cloud accounts  
2. Pre-authorised isolation capability and MTTI measurement on Tier-0  
3. Toxic-combination detection and continuous exposure view  
4. KEV-first remediation with automated validation  
5. AI agent and vendor governance as privileged identities  
6. Decision-rights SLAs and skills-as-risk controls

### Suggested Metrics

- Mean Time to Isolate (MTTI) on Tier-0  
- Open KEV count and age on internet-facing and Tier-0 systems  
- Open toxic combinations on crown-jewel assets (with owners)  
- Percentage of vendor/service/AI-agent credentials with owner, expiry, and last-use  
- Credentials older than project end date (target: zero)  
- Decision latency breaches

These controls are prioritised by how breaches are actually occurring in 2026, not by traditional compliance checklists.
