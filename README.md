# 🌍 ESG Multi-Agent Sustainability Auditor
![Dark workflow canvas showing a Lead Sustainability Auditor node at the top routing incoming environmental data to three connected agents below: Scope 3 Agent for supply chain emissions, vendor transport, shipping, and employee travel; Scope 1 Agent for direct emissions from company-owned vehicles, facilities, and fuel; and Scope 2 Agent for indirect emissions from purchased electricity and heating. The interface shows Flow, Schedule, Preview, and Update controls around the organized node diagram.](system_flow-1.png)
## Overview
The **ESG Multi-Agent Sustainability Auditor** is an automated, event-driven enterprise AI architecture designed to classify, route, and calculate corporate greenhouse gas (GHG) emissions. Built using Google Cloud Gemini Enterprise Agent Platform, this system eliminates manual data sorting by orchestrating a network of specialized AI agents that independently process Scope 1, Scope 2, and Scope 3 environmental data.

By decentralizing the audit process into specialized sub-agents, this architecture delivers high fault tolerance, scalable data ingestion, and precise emission calculations compliant with standard GHG protocols.

## 🏗️ System Architecture

This project utilizes a **Router-Worker** multi-agent design pattern. An entry-point Lead Auditor handles intent recognition and securely routes unstructured data to domain-specific calculation agents.

| Agent Role | Domain Specialty | Primary Function |
| :--- | :--- | :--- |
| **Lead Sustainability Auditor** | Traffic Routing | Analyzes raw input (invoices, logs, bills) and routes context to the appropriate worker agent based on emission type. |
| **Scope 1 Agent** | Direct Emissions | Calculates $CO_2e$ from company-owned assets, facility boilers, and fleet fuel consumption. |
| **Scope 2 Agent** | Indirect Energy | Extracts kWh data from utility bills and applies regional eGRID emission factors to calculate purchased energy footprint. |
| **Scope 3 Agent** | Supply Chain & Travel | Evaluates complex supply chain logs, vendor transport, and employee business travel data. |

## 🚀 Key Enterprise Value
* **Automated Data Triage:** Replaces manual HR/Sustainability categorization by automatically parsing unstructured vendor invoices and utility bills.
* **Domain Specialization:** Each sub-agent is strictly bounded to its specific emission scope, preventing hallucinations and logic crossover between direct and indirect calculation formulas.
* **Auditability:** Maintains a clear routing log and calculation rationale for every transaction, ensuring compliance readiness for ESG reporting.

## 📁 Repository Structure
```text
esg-multiagent-auditor/
├── lead_router_prompt.md    # System prompt for the primary router
├── scope_agents_config.yaml # YAML configurations for the worker network
├── system_flow.png          # Architecture visual map
└── README.md                # Documentation
```

🛠️ Tech Stack
- Orchestration: Google Cloud Gemini Enterprise Agent Platform

- LLM Engine: Gemini 3.8 Flash

- Architecture: Multi-Agent Routing (Zero-Code Workspace)
