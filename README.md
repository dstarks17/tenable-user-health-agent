# Tenable User Health Agent

A Claude Code agent that generates user management and authentication security health reports from Tenable Vulnerability Management. It audits user activity, authentication patterns, API key usage, and compliance posture against NIST 800-53 controls focused on least privilege and access management.

## What It Does

- Audits user activity and inactivity patterns
- Analyzes authentication methods (password, API key, SSO, MFA)
- Detects failed authentication attempts and brute-force indicators
- Assesses API key usage patterns and source IPs
- Evaluates separation of duties and least privilege
- Maps findings to NIST 800-53 controls (AC-5, AC-6, AC-7, IA-2, IA-4, IA-5, AU-2, SI-4)

## Requirements

- Claude Code with the Tenable MCP server connected
- Access to Tenable Vulnerability Management audit logs

## Usage

This agent runs inside Claude Code. Once installed, invoke it when you need to:

- Assess user hygiene across your Tenable environment
- Verify authentication controls are properly configured
- Prepare for a compliance review
- Identify inactive or over-privileged accounts

## Output

Generates a structured report including:

1. Summary table with risk-rated findings
2. Per-user authentication and access profiles
3. Authentication security findings
4. Least privilege assessment
5. Prioritized recommendations with NIST control mappings
6. Compliance status against relevant NIST 800-53 controls
7. Data gaps and mitigation suggestions
