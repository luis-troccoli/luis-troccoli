## Hi, I'm Luis 👋 — I make clouds boring (for attackers) 🔐☁️

```hcl
resource "engineer" "luis" {
  role       = "Cloud Security Engineer | DevSecOps"
  path       = "UX/UI → web dev → cloud security"
  clouds     = ["azure", "gcp", "aws"]
  languages  = ["es", "en", "it"]

  security {
    network_default        = "deny"
    static_credentials     = 0
    unscanned_deploys      = false
    budget_alerts_at       = [50, 75, 90, 100]
  }

  lifecycle {
    prevent_destroy = true  # runs on coffee
  }
}
```
```
$ terraform plan
Plan: 1 engineer to add, 0 to change, 0 secrets to leak.
```

### 🧠 How I think

Security that slows developers down gets bypassed. So I build guardrails that run *inside* the workflow: modular Terraform, default-deny networks, secrets in the platform's native vault, and CI/CD where a failed security scan **blocks** the merge instead of printing a warning nobody reads.

I've spent 6+ years in cloud infrastructure, SOC operations and security automation, and I started in UX/UI and web development. That's why I care whether infrastructure is *reviewable*: clear module boundaries, no hidden defaults, nothing you need me in the room to understand.

### 🚩 5 things I'll flag in your repo in the first five minutes

1. **Long-lived cloud keys in CI secrets.** Use OIDC / Workload Identity Federation. Credentials that don't exist can't leak.
2. **A security scanner that only warns.** If Checkov can't fail the build, it's decoration.
3. **`0.0.0.0/0` "just for testing".** It's never just for testing.
4. **`"Action": "*"` anywhere near IAM.** Least privilege isn't a phase-two task.
5. **No budget alerts.** A runaway resource is a security incident that bills you monthly.

### 🧪 What I've built

| Project | What it does | Stack |
| --- | --- | --- |
| [**SolSOC**](https://github.com/luis-troccoli/solsoc) | AI SOC alert triage: verdict, severity, MITRE ATT&CK mapping and next action for every alert. ~$0.04 per 5-alert run, cheaper than the analyst's coffee. | Python · Splunk · Sentinel · Wazuh · OpenAI / Claude / Gemini |
| [Project Vault](https://github.com/luis-troccoli/project-vault) | **Phase 1:** Azure security fundamentals, a hardened Key Vault and default-deny NSGs | Terraform · Key Vault · RBAC · NSG |
| [Secure Cloud Foundation](https://github.com/luis-troccoli/secure-cloud-foundation) | **Phase 2:** federated identity and shift-left security, zero static credentials | GitHub Actions · OIDC · Checkov |
| [FinTech-Guard-OS](https://github.com/luis-troccoli/fintech-guard-os) | **Phase 3:** modular Azure architecture with FinOps guardrails | Terraform modules · Azure Budgets |
| [FinTech-Guard-Native](https://github.com/luis-troccoli/gcp-fintech-guard-native) | The same baseline on Google Cloud, with notes where guardrails don't translate 1:1 | Terraform · Secret Manager · Workload Identity Federation |

### 🔭 Right now
- Bringing the baseline to **AWS**, the third cloud
- Making SolSOC smarter about what *not* to escalate
- 💬 Ask me about Terraform guardrails, CI/CD security gates or FinOps budgeting

### 🛠️ Toolbox

![Azure](https://img.shields.io/badge/azure-%230072C6.svg?style=for-the-badge&logo=microsoftazure&logoColor=white) ![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white) ![Google Cloud](https://img.shields.io/badge/GoogleCloud-%234285F4.svg?style=for-the-badge&logo=google-cloud&logoColor=white) ![Terraform](https://img.shields.io/badge/terraform-%235835CC.svg?style=for-the-badge&logo=terraform&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/github%20actions-%232671E5.svg?style=for-the-badge&logo=githubactions&logoColor=white) ![Splunk](https://img.shields.io/badge/splunk-%23000000.svg?style=for-the-badge&logo=splunk&logoColor=white) ![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white) ![Kubernetes](https://img.shields.io/badge/kubernetes-%23326ce5.svg?style=for-the-badge&logo=kubernetes&logoColor=white) ![PowerShell](https://img.shields.io/badge/PowerShell-%235391FE.svg?style=for-the-badge&logo=powershell&logoColor=white) ![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)

<sub>Also fluent in: React · Next.js · Node.js · TypeScript · Tailwind · MySQL · Adobe Creative Suite, from the web-and-design years.</sub>

---

[LinkedIn](https://www.linkedin.com/in/luis-troccoli-it/) · 🇪🇸 🇬🇧 🇮🇹
