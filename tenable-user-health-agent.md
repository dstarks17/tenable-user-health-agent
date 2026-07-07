---
name: "Tenable User Health Agent"
author: "dstarks17"
github_url: "https://github.com/dstarks17/tenable-user-health-agent"
description: "Claude Code agent that audits Tenable user activity, authentication patterns, and compliance posture across 6 frameworks"
license: "MIT"
type: "agent"
tier: "unreviewed"
tags: [user-management, authentication, compliance, audit, tenable, identity-access]
framework: "Claude Code"
integrations: [Tenable]
date_added: 2026-07-07
---

A Claude Code agent that generates comprehensive user management and authentication security health reports from the Tenable One platform.

## What it does

- Audits user activity and inactivity patterns across Tenable Vulnerability Management
- Analyzes authentication methods (password, API key, SSO, MFA) and detects failed login attempts
- Assesses API key usage patterns, source IPs, and separation of duties
- Evaluates least privilege and identifies over-privileged or inactive accounts
- Maps all findings to your chosen compliance framework(s): NIST 800-53, CIS Controls v8, ISO 27001, SOC 2, PCI DSS, and HIPAA

## How it works

The agent queries the Tenable audit log and platform configuration via the Tenable MCP server, collecting authentication events, session data, configuration changes, and resource ownership. It builds per-user profiles assessing risk indicators like shared credentials, multi-IP API key usage, and admin actions without MFA. Output is a structured markdown or HTML report with risk-rated findings, prioritized recommendations, and compliance control mappings.
