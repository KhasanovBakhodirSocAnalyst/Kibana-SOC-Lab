# VPN Connection Log Analysis

## 1. Investigation Overview

This investigation focused on analyzing VPN connection logs using **Elastic Kibana Discover**. The objective was to establish a baseline for the available VPN activity before performing more targeted searches and filtering.

The investigation used the `vpn_connections` index and a defined time window covering **31 December 2021 through 2 February 2022**.

## 2. Objective

The primary objectives were to:

* Identify the total volume of VPN connection events within the selected period.
* Establish a baseline for subsequent investigation.
* Become familiar with Kibana Discover and indexed security log data.
* Practice time-based filtering as part of a SOC investigation workflow.

## 3. Investigation Environment

| Item               | Details                           |
| ------------------ | --------------------------------- |
| Platform           | Elastic Kibana                    |
| Interface          | Discover                          |
| Index              | `vpn_connections`                 |
| Data Type          | VPN connection logs               |
| Time Range         | 31 Dec 2021 – 2 Feb 2022          |
| Investigation Type | Log analysis / SIEM investigation |

## 4. Investigation Procedure

### Step 1 — Select the Data Source

Opened **Kibana Discover** and selected the:

`vpn_connections`

index.

### Step 2 — Define the Investigation Time Range

Configured the time range to:

`31 December 2021 → 2 February 2022`

This ensured that the investigation was limited to the required period.

### Step 3 — Review Available Events

Reviewed the returned documents and the event distribution shown in the Kibana Discover interface.

The time-series visualization provided an initial view of VPN activity across the selected period.

### Step 4 — Establish the Event Baseline

Reviewed the total number of matching events returned by Elasticsearch.

## 5. Result

**Total VPN connection events: 2,861**

This establishes the initial dataset size for the investigation.

## 6. Evidence

The Kibana Discover interface was used as the primary investigation interface.

![Kibana VPN Connection Log Analysis](../screenshots/01-vpn-connections-time-range.png)

The screenshot demonstrates:

* `vpn_connections` index selection
* Defined investigation time range
* Total event count
* VPN event distribution over time
* Individual VPN connection records

## 7. SOC Analyst Analysis

Establishing an event baseline is an important first step in SIEM-based investigation.

The total of **2,861 events** provides context for subsequent analysis. Instead of investigating individual events without context, an analyst can use this baseline to identify unusual patterns, high-volume sources, unusual users, or activity spikes.

The next stages of the investigation can therefore focus on specific fields such as:

* `Source_ip`
* `UserName`
* `Source_Country`
* `source_state`
* `action`
* `protocol`
* `port`
* `@timestamp`

These fields can be correlated and filtered to identify potentially suspicious VPN activity.

## 8. Security Investigation Workflow

This task represents the initial stage of a typical SOC investigation:

**Data Source → Time Filtering → Event Baseline → Targeted Investigation**

The same workflow can be applied to other security data sources such as Windows Event Logs, authentication logs, firewall logs, endpoint telemetry, and network traffic.

## 9. Skills Demonstrated

* Elastic Kibana Discover
* Elasticsearch index analysis
* SIEM log analysis
* Time-range filtering
* VPN log investigation
* Event-volume analysis
* Security data interpretation
* Investigation documentation
* SOC investigation workflow

## 10. Lab Source

Hands-on investigation performed using the **TryHackMe Investigating with ELK 101** lab environment.

This documentation records my own investigation process and findings.
