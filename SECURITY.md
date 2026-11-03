# Security Policy

## Overview
The **Charge-Limit-Magisk-Module** operates at root level within Android sysfs interfaces (`/sys/class/power_supply/`) to manage charge control and battery thresholds. Because this module interacts directly with system level files and power control nodes, security and stability are paramount.

---

## Supported Versions

Please refer to the table below for security update support status for various module releases:

| Version | Supported          | Notes                                     |
| ------- | ------------------ | ----------------------------------------- |
| `v1.x`  | :white_check_mark: | Currently maintained for security updates |
| `< 1.0` | :x:                | Deprecated                                |

---

## Reporting a Vulnerability

If you discover a security vulnerability, unexpected root escalation, or dangerous sysfs manipulation issue in this module, please follow responsible disclosure practices.

### Process
1. **Do NOT open a public issue** on GitHub for sensitive security vulnerabilities.
2. Send an email to the repository owner or submit a private security advisory via [GitHub Security Advisories](https://github.com/Jamagoze/Charge-Limit-Magisk-Module/security/advisories/new).
3. Include the following details in your report:
   - Module version and Magisk/Kernel environment (e.g., KernelSU, APatch, Magisk version).
   - Target device and Android version.
   - Steps to reproduce the issue.
   - Potential impact or privilege escalation risks.

### Response Time
- **Acknowledgment:** Within 48 hours of report submission.
- **Assessment & Triage:** Within 5 business days.
- **Fix & Disclosure:** Patch released as soon as possible after verifying the fix.

---

## Scope & Security Considerations

### What is covered:
- Unauthorized privilege escalations via scripts included in the module.
- Malicious or unsafe writes to system files outside of designated charging nodes.
- Execution vulnerabilities within terminal/shell wrappers provided by the module.

### What is NOT covered (Out of Scope):
- Issues resulting from third-party modified versions or forks of this module.
- Known limitations or vulnerabilities in Magisk, KernelSU, APatch, or underlying Android kernels.
- Hardware damages resulting from user-defined current/voltage overrides beyond device safety specifications.
