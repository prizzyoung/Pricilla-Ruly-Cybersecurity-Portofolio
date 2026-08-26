# Incident Overview

Incident Type: Endpoint Security Alert

Security Function: Security Monitoring & Incident Response

Detection Sources: SIEM & CrowdStrike

Role: SOC / IT Security Analyst

Status: Resolved

# Executive Summary

A security alert was identified through the organization's security monitoring environment and correlated with endpoint telemetry from CrowdStrike.

The alert was investigated to determine whether the activity represented legitimate user behavior, a false positive, or potentially malicious activity.

The investigation involved reviewing the alert context, affected endpoint, user activity, process information, and related security events. Based on the investigation results, appropriate containment and remediation actions were performed.

This case demonstrates the end-to-end workflow of security monitoring, alert triage, investigation, containment, remediation, and incident reporting

# Detection

The activity was initially identified through security monitoring.

The SIEM was used to review and correlate security events, while CrowdStrike provided endpoint-level telemetry and visibility into the affected host.

The investigation focused on:

* Alert severity and detection type.
* Affected endpoint.
* User associated with the activity.
* Process and execution context.
* Related security events.
* Timeline of activity.
* Indicators associated with the alert.

## Investigation Workflow

The investigation followed a structured SOC workflow:

Security Alert
      ↓
Initial Triage
      ↓
Validate Alert Context
      ↓
Identify Affected Endpoint
      ↓
Review CrowdStrike Telemetry
      ↓
Correlate Events in SIEM
      ↓
Determine Threat Severity
      ↓
Containment
      ↓
Remediation
      ↓
Validation
      ↓
Incident Reporting

# Incident Response

Following the investigation, response actions were performed based on the assessed risk.

Potential response actions included:

## 1. Containment
* Isolate the affected endpoint where required.
* Prevent further execution of identified malicious activity.
* Restrict potentially compromised resources.
## 2. Remediation
* Quarantine identified suspicious files.
* Remove or remediate malicious artifacts.
* Purge quarantined files where appropriate.
* Review persistence mechanisms.
* Validate endpoint security status.
## 3. Recovery
* Confirm the endpoint returned to a healthy state.
* Verify that the suspicious activity was no longer observed.
* Continue monitoring for recurrence.

# Security Awareness

> An alert is not an incident until it has been investigated and understood.

Effective SOC operations require more than simply monitoring dashboards.

The analyst must be able to triage, correlate, investigate, respond, validate, and document security events.

A low-severity alert may become significant when correlated with other events, while a high-severity alert may ultimately be determined to be a false positive.

# Conclusion

This case demonstrates an end-to-end SOC monitoring and incident response workflow, combining centralized SIEM visibility with endpoint telemetry from CrowdStrike.

The investigation focused on understanding the context behind the alert, correlating related events, identifying the affected endpoint, performing appropriate containment and remediation, and validating the environment after response.

The key takeaway is:

> Detect → Triage → Investigate → Correlate → Contain → Remediate → Validate → Report
