# ghost-data-audit-agent
# AI-Powered Data Compliance & Deletion Audit Agent

An intelligent, object-oriented Python audit agent designed to detect "ghost data" and audit customer deletion requests for compliance. Built for high-throughput forensic analysis of distributed system logs, database replicas, and security evidence.


##  Key Features

* **Automated Forensic Analysis**: Cross-references customer deletion requests (`deletion_requests.csv`) with operational system logs (`system_activity.csv`) and deep forensic evidence repositories.
* **Deep Evidence Parsing**: Recursively scans and parses nested directory structures (`datasets/`, `documents/`, `images/`, `logs/`, `records/`) to inspect internal file payloads for unredacted records and failover anomalies.
* **Structured Compliance Pipeline**: Evaluates cases against company compliance rules (`deletion_rules.csv`) and assigns precise statuses (`COMPLETE`, `INCOMPLETE`, `NOT_APPLICABLE`).
* **Standardized Remediation Schema**: Generates structured JSON remediation steps strictly ordered by phases: `FINDING` $\rightarrow$ `REMEDIATION` $\rightarrow$ `VERIFICATION`.


##  Tech Stack

* **Language**: Python 3.x
* **Data Processing**: Pandas
* **File System Operations**: OS, JSON, CSV handling
* **Architecture**: Object-Oriented Programming (OOP) with dynamic relative path resolution


##  Project Structure

```text
├── code/
│   └── agent.py          # Core auditing agent implementation
├── dataset/
│   ├── deletion_requests.csv
│   ├── deletion_rules.csv
│   ├── system_activity.csv
│   └── evidence/         # Nested forensic evidence repository
├── output.csv            # Generated compliant audit report
└── README.md
