# Tenable User Health Agent

A Claude Code agent that generates user management and authentication security health reports from the Tenable One platform. It audits user activity across the platform — including Vulnerability Management, Cloud Security, Identity Exposure, and other Tenable One modules — analyzing authentication patterns, API key usage, and compliance posture against multiple industry frameworks.

## What It Does

- Audits user activity and inactivity patterns
- Analyzes authentication methods (password, API key, SSO, MFA)
- Detects failed authentication attempts and brute-force indicators
- Assesses API key usage patterns and source IPs
- Evaluates separation of duties and least privilege
- Maps findings to your chosen compliance framework(s)

## Requirements

- Claude Code with the Tenable MCP server connected
- Access to Tenable One platform audit logs

## Usage

This agent runs inside Claude Code. Once installed, invoke it when you need to:

- Assess user hygiene across your Tenable environment
- Verify authentication controls are properly configured
- Prepare for a compliance review
- Identify inactive or over-privileged accounts

## Supported Compliance Frameworks

The agent can map findings to one or more of the following frameworks. If no framework is specified, it will ask which to use (or default to NIST 800-53 for a quick run).

| Framework | Focus Areas |
|-----------|-------------|
| **NIST 800-53** | AC-5, AC-6, AC-7, IA-2, IA-4, IA-5, AU-2, SI-4 |
| **CIS Controls v8** | Controls 5, 6, 8 — account management, access control, audit logs |
| **ISO 27001:2022** | A.5.15–A.5.18, A.8.2, A.8.3, A.8.5, A.8.15 |
| **SOC 2** | CC6.1–CC6.3, CC6.6, CC7.1, CC7.2 |
| **PCI DSS v4.0** | Requirements 7 & 8 — access restriction, authentication |
| **HIPAA Security Rule** | 164.312(a), (b), (d); 164.308(a)(3)–(5) |

Multiple frameworks can be selected simultaneously for a unified cross-mapped report.

## Output

Generates a structured report including:

1. Summary table with risk-rated findings
2. Per-user authentication and access profiles
3. Authentication security findings
4. Least privilege assessment
5. Prioritized recommendations with control mappings
6. Compliance status against selected framework(s)
7. Data gaps and mitigation suggestions
