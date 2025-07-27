# OSINT Domain Reconnaissance Tool

A Docker-based OSINT (Open-Source Intelligence) domain reconnaissance tool that runs theHarvester and Amass in parallel to gather comprehensive domain intelligence.

## Features

- **Parallel Execution**: Runs theHarvester and Amass concurrently for faster results
- **Deduplication**: Automatically removes duplicate findings across tools
- **Multiple Output Formats**: Supports stdout (human-readable) and Excel (XLSX) output
- **Persistent Storage**: Saves scan results for later retrieval
- **Docker Containerization**: Easy deployment and isolation

## Prerequisites

- Docker installed on your system
- At least 2GB of available RAM
- Internet connection for tool downloads

## Building the Docker Image

```bash
docker build -t osint-scanner .
```

## Usage

The tool has two mutually exclusive modes of operation:

### 1. Scanning Mode

Run a new OSINT scan against a domain:

```bash
# Scan with stdout output
docker run osint-scanner -o stdout google.com

# Scan with Excel output
docker run osint-scanner -o excel google.com
```

### 2. Retrieval Mode

Retrieve results from a previous scan using the scan ID:

```bash
# Retrieve with stdout output
docker run osint-scanner -o stdout a1b2c3d4

# Retrieve with Excel output
docker run osint-scanner -o excel a1b2c3d4
```

## License

This project is for educational and authorized security testing purposes only. 