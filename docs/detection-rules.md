
# Windows Authentication Detection Rules

## Purpose

Define detection logic for identifying suspicious Windows authentication activities.

These rules are initial detection hypotheses and will be validated against the collected dataset.

## Rule 1: Multiple Failed Login Attempts

- Event ID: 4625
- Severity: Medium
- Description: Detect repeated failed login attempts from the same source IP address.
- Initial Threshold: 5 or more failures within 5 minutes.
- Investigation: Review source IP, target account, timestamps, and failure reasons.

## Rule 2: Failed Logins Followed by Successful Login

- Event IDs: 4625, 4624
- Severity: High
- Description: Identify a successful login following multiple failed attempts.
- Initial Threshold: 5 or more failures followed by a successful login within 10 minutes.
- Investigation: Review the account, source IP, logon type, and event sequence.

## Rule 3: Account Lockout

- Event ID: 4740
- Severity: Medium
- Description: Identify accounts locked after repeated authentication failures.
- Investigation: Review the affected account and caller computer name.

## Investigation Guidelines

For each alert, record:

- Timestamp
- Username
- Source IP address (when available)
- Event ID
- Number of failed attempts
- Detection rule
- Severity
- Investigation findings
- Recommended response

## Important Notes

- Thresholds are initial values and must be validated against the dataset.
- Event fields may differ depending on the log source.
- A detection alert does not automatically confirm malicious activity.
