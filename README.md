# mini-soc-investigation
# Mini SOC Investigation: Log and Network Correlation

## 📌 Project Overview
This project simulates a real-world Security Operations Center (SOC) investigation by analyzing and correlating network traffic and system logs to identify suspicious activity and potential attack behavior.

The goal was to practice SOC analyst skills such as log analysis, traffic inspection, attack pattern recognition, and incident response thinking.

---

## 🛠️ Tools & Technologies
- Linux (Kali Linux)
- Wireshark
- Linux command-line tools
- System and authentication logs

---

## 🔍 Investigation Scenario
During routine monitoring, repeated HTTP requests returning error responses were observed from a single IP address. Shortly after, multiple failed SSH login attempts were detected originating from the same source.

This activity was analyzed to determine whether it represented normal behavior or a coordinated attack.

---

## 🧪 Analysis Performed

### Network Traffic Analysis
- Captured live network traffic using Wireshark
- Inspected HTTP traffic and identified repeated `GET` requests resulting in `404 Not Found` responses
- Interpreted the activity as automated web scanning or resource enumeration
- Analyzed TCP session behavior to confirm legitimate vs suspicious traffic patterns

### Log Analysis
- Reviewed Linux authentication logs to identify failed SSH login attempts
- Correlated timestamps and source IP addresses with observed network activity
- Identified repeated authentication failures indicating attempted unauthorized access

---

## 🚨 Findings
- Repeated HTTP 404 responses from a single IP indicated reconnaissance activity
- Subsequent failed SSH login attempts suggested an escalation from reconnaissance to access attempts
- The behavior matched a common attack chain: **Reconnaissance → Access Attempt**

---

## 🛡️ Recommended Response Actions
- Temporarily block or rate-limit the source IP
- Review SSH configuration and restrict access to authorized users
- Continue monitoring logs for successful authentication attempts
- Preserve logs for further forensic analysis

---

## 🎯 Skills Demonstrated
- Network traffic analysis
- Log analysis and event correlation
- Threat detection and attack chain identification
- SOC-style incident response thinking
- Linux security fundamentals

---

## 📚 Key Takeaway
This project demonstrates the importance of correlating multiple data sources—network traffic and system logs—to accurately detect and respond to security incidents in a SOC environment.
