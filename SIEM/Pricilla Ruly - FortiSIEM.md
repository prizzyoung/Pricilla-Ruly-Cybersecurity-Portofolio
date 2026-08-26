# Incident Overview

Incident Type: Suspicious Network Activity / Security Event

Security Function: Security Monitoring & Incident Response

Detection Platform: FortiSIEM

# Executive Summary

A suspicious security event was identified through FortiSIEM, the organization's centralized Security Information and Event Management (SIEM) platform.

FortiSIEM was used to collect, normalize, correlate, and analyze security events from multiple sources. The investigation focused on identifying the source of the activity, understanding the affected systems, analyzing the event timeline, and determining whether the activity represented a legitimate event or a potential security incident.

The investigation followed a structured SOC workflow covering monitoring, alert triage, event correlation, investigation, response, and reporting.
<img width="1336" height="500" alt="image" src="https://github.com/user-attachments/assets/57cc0446-187f-464c-ba43-132a50648cc4" />

# Event Correlation

One of the key capabilities used during the investigation was event correlation.

Instead of analyzing a single log entry in isolation, related events were grouped based on common attributes such as:

* Source IP.
* Destination IP.
* Username.
* Host.
* Event type.
* Timestamp.
* Network service.

# Conclusion

This case demonstrates the use of FortiSIEM for centralized security monitoring, log analysis, event correlation, and incident response.

The investigation went beyond reviewing individual alerts by correlating related events and analyzing the activity from an attacker-oriented perspective.

The overall SOC workflow can be summarized as:

Detect → Triage → Analyze → Correlate → Investigate → Respond → Validate → Report
