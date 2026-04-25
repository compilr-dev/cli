# Security Policy

We take security seriously across the compilr.dev ecosystem. If you believe you've found a vulnerability in this project, **please do not file a public GitHub issue** — disclosure of unpatched issues puts users at risk.

## Reporting a Vulnerability

Email **hello@compilr.dev** with `[SECURITY]` in the subject line, and include:

- A description of the issue and the impact (what an attacker could do)
- Steps to reproduce, ideally including a minimal test case
- The version(s) you confirmed it on
- Your contact info if you'd like credit in the fix

We aim to acknowledge reports within **3 business days** and provide a status update within **7 days**. Critical vulnerabilities are typically patched and released within **14 days** of confirmation; lower-severity issues may take longer.

## Disclosure

Once a fix is released we'll publish an advisory through GitHub's security advisory system (and a CVE where appropriate), credit the reporter (unless you ask us not to), and reference the patched version in our changelog.

## Scope

This policy covers code shipped from this repository (or from the corresponding npm package) at its currently-published version. Issues in transitive dependencies should be reported upstream; we'll happily cooperate on coordinated fixes.

## Out of Scope

- Self-XSS or social-engineering scenarios that require an attacker to trick a user into pasting malicious input into their own session
- Issues that depend on a compromised user machine (extracted credentials, malicious npm install, etc.) — these are real threats but outside what this code can defend against
- Vulnerabilities in third-party services we integrate with (Anthropic, OpenAI, Supabase, Netlify, etc.) — please report those to the respective vendors

## Alternative Channels

You can also report via [GitHub's private vulnerability reporting](https://docs.github.com/en/code-security/security-advisories/guidance-on-reporting-and-writing-information-about-vulnerabilities/privately-reporting-a-security-vulnerability) on this repository — open the **Security** tab and click **Report a vulnerability**.

Thank you for helping keep compilr.dev users safe.
