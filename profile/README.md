<div align="center">
  <img src="https://lorikeetsecurity.com/images/lorikeet-logo-banner.png" width="150px" alt="Lorikeet Security" />
  <br /><br />
  <strong>Lorikeet Security</strong><br />
  <sub>Human first. AI-native. One platform for your whole security program.</sub>
  <br /><br />
  <a href="https://lorikeetsecurity.com">Website</a> &nbsp;·&nbsp;
  <a href="https://lorikeetsecurity.com/lory">Lory</a> &nbsp;·&nbsp;
  <a href="https://lorikeetsecurity.com/ptaas">Talon</a> &nbsp;·&nbsp;
  <a href="https://lorikeetsecurity.com/developers">Docs</a> &nbsp;·&nbsp;
  <a href="https://lorikeetsecurity.com/blog">Research</a> &nbsp;·&nbsp;
  <a href="https://www.linkedin.com/company/lorikeetsecurity">LinkedIn</a> &nbsp;·&nbsp;
  <a href="https://x.com/lorikeetsec">X</a>
</div>

---

We run human-led penetration tests and an autonomous AI pentester against the same scope, and every finding either agent produces is countersigned by a human before it reaches a client. This org is where the open-source half of that lives: the scanner your developers run locally, the cockpit they triage from, the agent you install inside your network, the labs we train on, and the tooling we build for our own engagements.

**We test the way attackers think. Then we help you fix it.**

---

### Where Lory Meets Your Code

Four surfaces, one AI pentester. Scan before you commit, triage findings from your terminal, run in-network posture sensors, or catch vulnerabilities in your editor.

| Project | What it does | |
|---|---|---|
| **[lory-cli](https://github.com/Lorikeet-Security/lory-cli)** | Official CLI for Lory, Lorikeet Security's autonomous AI pentester and Talon PTaaS platform. Built in Go with Cobra and Bubbletea TUI, featuring Docker worker sandboxing, local MCP integration, and Talon SSO. | `Go` `Apache 2.0` |
| **[vs-code](https://github.com/Lorikeet-Security/vs-code)** | Lory reviews your code for vulnerabilities as you write it, inside VS Code. Catch security issues at the keystroke, not at the pentest. [Available on the Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=LorikeetSecurity.lory). | `TypeScript` `Marketplace` |
| **[lory-findings-tui](https://github.com/Lorikeet-Security/lory-findings-tui)** | Findings triage and AI-assisted remediation in your terminal. Pull Lorikeet Security findings, trace them to your code, ask Lory for the fix, and file a retest. | `Python` `MIT` |
| **[lory-code-security-scanner](https://github.com/Lorikeet-Security/lory-code-security-scanner)** | AI-powered static code security scanner. Finds vulnerabilities across your codebase, validates them to cut false positives, and reports findings in an actionable format. | `Python` `MIT` |
| **[lorikeet-security-exporter](https://github.com/Lorikeet-Security/lorikeet-security-exporter)** | Agentic exporter and runner for internal network pentesting, autonomous host discovery, patch/vulnerability state collection, and server/application inventory. | `Python` `MIT` |

```bash
# Install the Lory CLI
curl -fsSL https://lorikeetsecurity.com/install.sh | bash

# Or install via Go
go install github.com/Lorikeet-Security/lory-cli@latest

# Run reviews, target audits, or pre-commit diffs
lory review .         # review current directory for vulnerabilities
lory scan target.com  # audit security headers, SSL/TLS, and posture
lory diff             # inspect staged git changes before commit
```

### Learn

| Project | What it does | |
|---|---|---|
| **[owasp-top-10-labs-lamp-dockerized](https://github.com/Lorikeet-Security/owasp-top-10-labs-lamp-dockerized)** | Dockerized OWASP Top 10 lab machines. Deliberately vulnerable, deliberately reproducible — what we train our own testers on. | `PHP` |

[**Browse all repositories →**](https://github.com/orgs/Lorikeet-Security/repositories)

---

### Bring Your Own Agent

Your security program shouldn't be locked behind our UI. Point Claude, Claude Code, or any MCP client at your own workspace:

```json
{
  "mcpServers": {
    "lorikeet": {
      "type": "http",
      "url": "https://lorikeetsecurity.com/ptaas/mcp/",
      "headers": { "Authorization": "Bearer <your-token>" }
    }
  }
}
```

Read access to findings, assets, compliance frameworks and control status, and the vulnerability knowledge base. One write action — request a retest. OAuth 2.1 with dynamic client registration, or a workspace API token. Every call is hard-scoped to the company that owns the credential. [MCP documentation →](https://lorikeetsecurity.com/mcp-docs)

---

### Security Research

**16 CVEs in FastNetMon Community Edition**, responsibly disclosed by our research team and indexed by NVD, Snyk, SentinelOne, Ubuntu and Vulners.

Two rated 9.8 Critical — a stack buffer overflow in BGP NLRI parsing ([CVE-2026-48686](https://lorikeetsecurity.com/blog/fastnetmon-cve-2026-48686-bgp-nlri-stack-overflow)) and an off-by-one heap overflow in dynamic buffer handling ([CVE-2026-48689](https://lorikeetsecurity.com/blog/fastnetmon-cve-2026-48689-dynamic-buffer-off-by-one)) — alongside command injection in the Juniper and MikroTik plugins, an unauthenticated gRPC control API, NetFlow and BGP parser over-reads, a symlink arbitrary file write as root, and missing TLS certificate validation.

[**Read the full disclosure series →**](https://lorikeetsecurity.com/blog) · [White papers](https://lorikeetsecurity.com/white-papers)

---

### Meet Lory

Lory is our AI pentester, not a chatbot with a security theme. She takes a signed scope, runs a deterministic sweep, picks her own attack vectors, gives each one a focused pass with its own budget, validates and chains what she finds, and drafts the finding — then a Lorikeet pentester countersigns it before it ever reaches you.

- **57 attack playbooks**, loaded one at a time — depth per vector instead of one giant prompt skimmed thin
- **1,969-entry knowledge base** built from OWASP ASVS, WSTG and Top 10, plus MITRE CWE and CAPEC
- **Nothing ships unreviewed.** Findings sit in `pending_review`, invisible even to you, until a human approves them
- **Every run reports its own gaps** — vectors planned, vectors run, and vectors cut short by the depth ceiling, with the reason attached
- **Prepaid credits, no seats.** $1 = 1 credit; MCP tool calls cost 0.1 credit; engagements bill by depth

[Meet Lory](https://lorikeetsecurity.com/lory) · [How a run works](https://lorikeetsecurity.com/lory#engagement) · [Coverage & gaps](https://lorikeetsecurity.com/lory#coverage)

---

### Working With Us

Penetration testing and red team · Autonomous testing with [Lory](https://lorikeetsecurity.com/lory) · Incident response and digital forensics · MDR and SOC-as-a-Service · SOC 2, ISO 27001, PCI DSS, HIPAA, CMMC · [vCISO](https://lorikeetsecurity.com/vciso) and VC due diligence

Everything runs through [**Talon**](https://lorikeetsecurity.com/ptaas) — findings stream in as we test, with evidence, remediation and free retesting. Findings route into Jira, GitHub, GitLab, Azure DevOps, Slack, Teams, Discord or a signed webhook, so the work starts where your engineers already are. Every run publishes what it covered *and* what it didn't.

[See an example report](https://lorikeetsecurity.com/example-report/Lorikeet_Demo_Report.pdf) · [Our methodology](https://lorikeetsecurity.com/methodology) · [Integrations](https://lorikeetsecurity.com/marketplace) · [Knowledge base](https://lorikeetsecurity.com/knowledge-base) · [Book a scoping call](https://lorikeetsecurity.com/contact#booking)

**Free, no sign-up:** [web security scanner](https://lorikeetsecurity.com/talon/tools/web-scanner) · [email security scanner](https://lorikeetsecurity.com/talon/tools/email-scanner) · [SSL checker](https://lorikeetsecurity.com/talon/tools/ssl-checker) · [DNS lookup](https://lorikeetsecurity.com/talon/tools/dns-lookup)

---

### Contributing & Disclosure

Issues and pull requests are welcome on any repo here. Keep collectors and rules modular and scope-safe, and include tests where practical.

Found a vulnerability in something we ship? Report it to **security@lorikeetsecurity.com** — we respond within one business day and we credit researchers. See our [Trust Center](https://lorikeetsecurity.com/trust-center) for scope and policy.

Everything in this org is for assessing systems you own or are explicitly authorized to test.

---

<div align="center">
  <sub>
    <a href="mailto:sales@lorikeetsecurity.com">sales@lorikeetsecurity.com</a> &nbsp;·&nbsp;
    <a href="https://lorikeetsecurity.com/careers">We're hiring</a>
    <br />
    Kissimmee, FL · New York, NY
    <br /><br />
    © 2021–2026 Lorikeet Corp, operating as Lorikeet Security
  </sub>
</div>
