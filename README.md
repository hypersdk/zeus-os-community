# Zeus os — Community

> **Visual operating system for Kubernetes — KubeVirt VMs, enterprise auth, cost optimization, 48+ TUI views**

Public issue tracker and community feedback space for **Zeus-os** by [Zyvor AI Labs](https://zyvor.dev).

The source code is maintained in a private repository. This repo is for:
- Bug reports
- Feature requests
- UX feedback
- Documentation gaps
- Questions and discussion

---

## Key features

- 48+ TUI views — k9s-style terminal interface for KubeVirt VMs
- Web dashboard — 48+ specialized pages at :5050
- VNC, serial, and SSH console proxies with live WebSocket metrics
- Per-VM cost tracking, waste detection, and forecasting
- Enterprise auth: OIDC/LDAP/SAML, scoped API tokens, session revocation
- Multi-tenant with namespace-scoped access
- Topology viewer, RCA engine, and guided remediation
- Velero DR integration and GitOps hooks

---

## Installation

**Helm:**
```bash
helm repo add hypersdk https://charts.hypersdk.dev
helm install zeus-os hypersdk/zeus-os -n zeus-system --create-namespace
# Web dashboard → http://localhost:5050
```

**Binary (Terminal UI):**
```bash
curl -fsSL https://releases.hypersdk.dev/zeus-os/install.sh | bash

# Terminal UI (k9s-style)
zeus-os
zeus-os production    # filter to a namespace

# Web dashboard
zeus-os-web           # http://localhost:5050
```

**Requirements:** Kubernetes 1.28+ with KubeVirt, OIDC provider (optional, for enterprise auth)

---

## Report a bug

[Open a Bug Report →](../../issues/new?template=bug_report.yml)

Include: what you did, what happened, what you expected, your environment, and screenshots/logs (redact secrets).

## Request a feature

[Open a Feature Request →](../../issues/new?template=feature_request.yml)

## UX feedback

[Open a UX Feedback →](../../issues/new?template=ux_feedback.yml)

## Ask a question

Use [GitHub Discussions](../../discussions) for open-ended questions, ideas, and roadmap conversations.

---

## Security

**Do not report security vulnerabilities publicly.**

Email **security@zyvor.dev** — see [SECURITY.md](SECURITY.md).

---

## Do not post

- Source code or internal configuration
- API tokens, license keys, or credentials  
- Private logs with sensitive data
- Security vulnerabilities (email security@zyvor.dev)

---

Maintained by [Zyvor AI Labs](https://zyvor.dev)
