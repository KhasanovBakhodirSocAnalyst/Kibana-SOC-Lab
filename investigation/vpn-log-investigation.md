## 1. VPN Connection Log Analysis

### Objective

Analyze VPN connection logs within a defined date range using Kibana Discover.

### Investigation

**Index selected:**
`vpn_connections`

**Time range:**
`31 December 2021 – 2 February 2022`

**Tool:**
Kibana Discover

### Procedure

1. Opened Kibana Discover.
2. Selected the `vpn_connections` index.
3. Set the time range from 31 December 2021 to 2 February 2022.
4. Reviewed the total number of matching log records (hits).

### Result

**Total hits:** `2,861`

### SOC Relevance

Establishing the number of events within a specific time window is an important first step in log investigation. It provides the analyst with the scope of available data before applying additional filters and investigating suspicious activity.

### Skills Demonstrated

- Kibana Discover
- Index selection
- Time-range filtering
- VPN log analysis
- Basic SIEM investigation
