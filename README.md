> 🚀 **Trial v0.30.0 is live!** The latest release is available for trial today — [get started in 5 minutes →](#try-v030-in-5-minutes)

# Zeus OS — Community

> **Visual operating system for Kubernetes — KubeVirt VMs, enterprise auth, cost optimization, 48+ TUI views.**

![Version](https://img.shields.io/badge/version-v0.30.0-blue) ![Discussions](https://img.shields.io/github/discussions/hypersdk/zeus-os-community) ![Issues](https://img.shields.io/github/issues/hypersdk/zeus-os-community) ![License](https://img.shields.io/badge/license-Proprietary-red)

Public issue tracker and community feedback space for **Zeus OS** by [Zyvor AI Labs](https://zyvor.dev).
The source code is maintained in a private repository. This repo is for bug reports, feature requests, UX feedback, and community discussion.

---

## What's new in v0.30

- 48 TUI views GA — full k9s-style terminal interface covering every KubeVirt resource type
- Per-VM cost dashboard — live cost tracking, waste detection, and 30-day forecasting in the web UI
- SAML SSO GA — enterprise identity provider integration alongside existing OIDC/LDAP support
- Velero DR one-click — trigger backup and restore workflows directly from the VM detail page
- WebSocket live metrics — CPU, memory, network, and disk metrics stream in real-time to the console

---

## Why Zeus OS

| Problem | Zeus OS answer |
|---------|---------------|
| KubeVirt ops require kubectl expertise most teams lack | Visual VM command center + 48-view TUI — no kubectl knowledge required |
| Cost per VM is invisible until month-end | Per-VM cost tracking, waste detection, and forecasting built into every view |
| Browser consoles are fragmented across tools | VNC, serial, SSH, and live WebSocket metrics — all in one dashboard |
| Enterprise needs auth and tenancy that KubeVirt lacks | OIDC/LDAP/SAML, scoped API tokens, per-namespace tenancy, session revocation |
| Incidents lack cross-layer context | Topology viewer, RCA engine, and guided remediation — from alert to fix in one screen |

---

## Architecture

```
┌──────────────────────────────────────────────────────────────┐
│  Surfaces     Web dashboard :5050 · TUI · 48+ specialized views│
├──────────────────────────────────────────────────────────────┤
│  Operations   VM lifecycle · consoles · hot-plug · migration │
├──────────────────────────────────────────────────────────────┤
│  Enterprise   OIDC/LDAP/SAML · tenants · audit · API tokens  │
└──────────────────────────────────────────────────────────────┘
```

---

## Try v0.30 in 5 minutes

```bash
# Helm
helm repo add hypersdk https://charts.hypersdk.dev
helm install zeus-os hypersdk/zeus-os --version 0.30.0 \
  -n zeus-system --create-namespace
# Web dashboard → http://localhost:5050

# Terminal UI (binary)
curl -fsSL https://releases.hypersdk.dev/zeus-os/install.sh | ZEUS_VERSION=0.30.0 bash
zeus-os                    # full TUI
zeus-os production         # filter to a namespace
zeus-os-web                # web dashboard on http://localhost:5050
```

**Requirements:** Kubernetes 1.28+ with KubeVirt, OIDC provider optional (for enterprise SSO)

---

## Report a bug

[Open a Bug Report →](../../issues/new?template=bug_report.yml)

Include: what you did, what happened, what you expected, your environment, screenshots or logs (redact secrets).

## Request a feature

[Open a Feature Request →](../../issues/new?template=feature_request.yml)

## UX feedback

[Open a UX Report →](../../issues/new?template=ux_feedback.yml)

## Ask a question

Use [GitHub Discussions](../../discussions) for open-ended questions, ideas, and roadmap conversations.

---

## Security

**Do not report security vulnerabilities publicly.**
Email **security@zyvor.dev** — see [SECURITY.md](SECURITY.md).

---

## Do not post

- Source code, internal configs, or architecture details
- API tokens, license keys, or credentials
- Private logs with sensitive data
- Security vulnerabilities — email security@zyvor.dev instead

---

## Join the community

⭐ [Star this repo](https://github.com/hypersdk/zeus-os-community) · 💬 [Open a Discussion](https://github.com/hypersdk/zeus-os-community/discussions) · 🐛 [Report a Bug](../../issues/new?template=bug_report.yml) · 📧 [hello@zyvor.dev](mailto:hello@zyvor.dev)

Maintained by [Zyvor AI Labs](https://zyvor.dev)
