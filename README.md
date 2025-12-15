# Threat Intelligence Framework

A comprehensive Python-based threat intelligence collection and enrichment framework designed for SOC teams and threat analysts.

## Features
- **Multi-source Intelligence Aggregation**: Collect indicators from VirusTotal, AlienVault OTX, URLhaus, and custom feeds
- **Enrichment Pipeline**: Automatic IP geolocation, WHOIS lookups, DNS resolution, SSL certificate analysis
- **MITRE ATT&CK Mapping**: Automatically classify threats using MITRE framework tactics and techniques
- **Risk Scoring**: ML-based scoring system for threat prioritization
- **API Integration**: RESTful API for integration with SIEM platforms (Splunk, ELK, Sentinel)
- **Reporting**: Automated reports with visualizations and actionable intelligence

## Installation
```bash
pip install threat-intel-framework
```

## Quick Start
```python
from threat_framework import ThreatIntelligence

ti = ThreatIntelligence()
ip = ti.analyze_ip("8.8.8.8")
print(ip.risk_score)
print(ip.mitre_techniques)
```

## Architecture
- Modular source collectors
- PostgreSQL backend for historical tracking
- Redis caching for performance
- Elasticsearch integration for large-scale analysis
- Grafana dashboards for visualization

## Use Cases
- Daily threat briefings
- Indicator prioritization
- Incident investigation support
- Threat hunting operations
- Security posture assessment