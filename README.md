# Network Intrusion Detection System (NIDS) using Suricata

## Project Overview

This project demonstrates the implementation of a Network Intrusion Detection System (NIDS) using Suricata on Kali Linux. The objective is to monitor network traffic, detect suspicious activities, generate alerts, and improve network security through continuous monitoring.

The project simulates how cybersecurity professionals deploy and configure intrusion detection systems to identify potential threats and malicious activities in real-world environments.

---

## Objectives

* Install and configure Suricata IDS.
* Monitor network traffic in real time.
* Detect suspicious or malicious network activity.
* Create and test custom detection rules.
* Generate alerts and logs for detected events.
* Analyze intrusion detection results.
* Document the implementation process and findings.

---

## Tools and Technologies Used

* Kali Linux
* Suricata IDS
* Terminal Commands
* Custom Rule Signatures
* Network Monitoring Utilities

---

## Project Architecture

Network Traffic
↓
Suricata Engine
↓
Detection Rules
↓
Alert Generation
↓
Log Analysis
↓
Security Monitoring

---

## Installation and Configuration

### Step 1: Verify Suricata Installation

```bash
suricata -V
```

### Step 2: Identify Network Interface

```bash
ip a
```

### Step 3: Configure Detection Rules

Custom rules were added to detect specific network activities and generate alerts.

Example Rule:

```text
alert icmp any any -> any any (msg:"ICMP Ping Detected"; sid:1000001; rev:1;)
```

### Step 4: Validate Configuration

```bash
sudo suricata -T -c /etc/suricata/suricata.yaml
```

### Step 5: Start Suricata

```bash
sudo systemctl start suricata
```

### Step 6: Verify Service Status

```bash
sudo systemctl status suricata
```

---

## Monitoring and Detection

The IDS continuously monitored network traffic and inspected packets using predefined detection signatures.

The system was configured to:

* Detect ICMP traffic
* Monitor suspicious network behavior
* Generate security alerts
* Record events in log files

---

## Custom Rules

The project includes custom Suricata rules stored in:

```text
suricata_rules.txt
```

Sample Rule:

```text
alert icmp any any -> any any (msg:"ICMP Ping Detected"; sid:1000001; rev:1;)
```

---

## Screenshots

The following screenshots are included in the project:

1. Suricata Installation Verification
2. Network Interface Configuration
3. Suricata Service Running
4. Alert Generation
5. Log Analysis

---

## Results

* Successfully installed Suricata IDS.
* Configured monitoring on the network interface.
* Implemented custom intrusion detection rules.
* Generated alerts for monitored activities.
* Verified intrusion detection functionality through testing.

---

## Security Benefits

* Early detection of suspicious activity.
* Continuous network monitoring.
* Improved visibility into network traffic.
* Enhanced incident response capability.
* Better overall network security posture.

---

## Challenges Faced

* Rule file configuration issues.
* Service configuration validation.
* Interface selection and monitoring setup.
* Log and alert verification.

All challenges were successfully resolved during project implementation.

---

## Future Enhancements

* Integration with SIEM platforms.
* Dashboard visualization for alerts.
* Automated incident response.
* Advanced threat detection signatures.
* Real-time notification system.

---

## Conclusion

This project successfully implemented a Network Intrusion Detection System using Suricata on Kali Linux. The system was able to monitor network traffic, detect suspicious activities, generate alerts, and demonstrate the importance of intrusion detection in modern cybersecurity environments. The project provided practical experience in network monitoring, threat detection, rule creation, and security analysis.
