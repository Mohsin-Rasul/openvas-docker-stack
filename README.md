
# Containerized OpenVAS Vulnerability Management Lab

## Overview
This repository provides a fully containerized deployment of OpenVAS (Greenbone Vulnerability Management) configured via Docker Compose. It is designed to quickly spin up a vulnerability scanning infrastructure for network security assessments, penetration testing, and security operations analysis. 

The project also includes a sample XML vulnerability report for analysis and testing purposes without needing to execute a live scan.

## Repository Structure
* **`compose.yaml`**: The Docker Compose configuration file orchestrating the OpenVAS services and dependencies.
* **`real_openvas_report.xml`**: A sample vulnerability assessment report exported directly from the scanner.
* **`Instructions.odt`**: Documentation and setup guidelines for deploying and utilizing the environment.
* **`LICENSE`**: Open-source licensing information.

## Prerequisites
To deploy this infrastructure, ensure you have the following installed on your host system:
* [Docker Engine](https://docs.docker.com/engine/install/)
* [Docker Compose](https://docs.docker.com/compose/install/)

## Quick Start Deployment

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/YourUsername/your-repo-name.git](https://github.com/YourUsername/your-repo-name.git)
   cd your-repo-name

```

2. **Deploy the stack:**
Execute the following command to download the necessary images and start the services in the background:
```bash
docker compose up -d

```


3. **Verify container health:**
Check the status of your deployment to ensure the OpenVAS manager, scanner, and web interface are running correctly:
```bash
docker compose ps

```



## Usage

Once the containers are successfully running, you can access the Greenbone Security Assistant (GSA) web interface (typically on port 9392, depending on your `compose.yaml` mapping).

From the dashboard, you can configure target networks, schedule automated scans, or import the provided `real_openvas_report.xml` to analyze the vulnerability findings, CVSS scores, and remediation steps.

```

---

Are you planning to integrate this containerized OpenVAS deployment with a SIEM like Wazuh or Splunk to centralize the vulnerability logs?

```
