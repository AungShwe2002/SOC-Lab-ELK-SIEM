# SOC Lab — ELK Stack SIEM

## Overview
ELK Stack (Elasticsearch, Logstash, Kibana) — SIEM Lab 

## Environment
- Ubuntu 24.04
- Elasticsearch 8.19.23
- Kibana 8.19.23
- WSL2

## Setup Steps
1. Elasticsearch Install
2. Kibana Install
3. Security On
4. Encryption Key Generate
5. Kibana Config — kibana_system Password
6. Data ထည့် — Dev Tools
7. Data View Create
8. Discover — Data ကြည့်
9. Visualization — Chart
10. Detection Rule — Brute Force
11. Alert — Security → Alerts

## Detection Rule
- **Rule Name** — Brute Force Detection
- **Query** — `event.code: "4625"`
- **Severity** — High
- **Risk Score** — 73
- **Schedule** — 5 minutes

## Test Data
```json
POST test-logs/_doc
{
  "@timestamp": "2026-10-16T14:00:00",
  "event": { "code": "4625" },
  "source": { "ip": "192.168.1.100" },
  "user": { "name": "testuser" }
}

Result

    Alerts — 58

    Severity — High

    Rule — Brute Force Detection

    Risk Score — 73

    Source IP — 192.168.1.100

    User — testuser

Screenshots

![Alerts Dashboard](https://github.com/user-attachments/assets/a5d4e9c9-0b15-4539-aea2-0e1e31292e0c)

Lessons Learned

    ELK Stack Setup

    Detection Rule Writing

    Alert Investigation

    Brute Force Detection

    KQL Query

Author

Aung Shwe


