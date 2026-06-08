# GCP Cloud Operations Monitoring Studio

This repository contains the target configuration and SRE runtime files compiled by the **GCP Cloud Operations Monitoring Studio** dashboard module.

## 🚀 Description
Design alert policies and dashboards for Google Cloud (Stackdriver). Generate MQL metric alerts, uptime checkpoints, and webhook warning routes.

## 🛠️ Specification Matrix
- **Primary Configuration File**: `/deploy/dashboards/metrics_dashboard.json`
- **Execution Command**: `gcloud monitoring dashboards create --config-from-file=metrics_dashboard.json`
- **Validation Command**: `gcloud monitoring dashboards list`

## 📋 How to Run & Validate

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Pradeeptalari14/tp-gcp-cloud-operations.git
   cd tp-gcp-cloud-operations
   ```

2. **Run Execution Target:**
   ```bash
   gcloud monitoring dashboards create --config-from-file=metrics_dashboard.json
   ```

3. **Verify Runtime Stability:**
   ```bash
   gcloud monitoring dashboards list
   ```

## 🔐 Security & Best Practices
* **Secret Isolation**: Use organization-level secrets (or SSM parameter hooks) rather than hardcoded environment variables inside files.
* **Pull Request Lifecycles**: Protect default branch merges with validation checks before merging code changes.
