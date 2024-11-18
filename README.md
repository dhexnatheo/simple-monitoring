# Simple Monitoring Stack

A lightweight and simple monitoring solution that uses [Telegraf](https://docs.influxdata.com/telegraf/v1/), [VMAgent](https://docs.victoriametrics.com/vmagent/), [Single-VictoriaMetrics](https://docs.victoriametrics.com/single-server-victoriametrics/), and [Grafana](https://grafana.com/grafana/) to monitor machine metrics and Docker containers. Each component runs in its own container, simplifying setup and configuration. Also, fully utilize docker-compose for deployment.

## Table of Contents

- [Simple Monitoring Stack](#simple-monitoring-stack)
  - [Table of Contents](#table-of-contents)
  - [Overview](#overview)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Usage](#usage)
  - [Configuration](#configuration)
    - [Environment Variables](#environment-variables)
    - [Configuring Telegraf](#configuring-telegraf)
    - [Grafana Dashboards](#grafana-dashboards)
  - [Reference](#reference)
  - [License](#license)

## Overview

This stack is designed to gather and visualize host system and container metrics. The monitoring stack includes:
- **Telegraf**: Collects system and container metrics.
- **VMAgent**: Serves as a scraping agent for Prometheus-compatible metrics.
- **VictoriaMetrics**: Stores the collected metrics in a scalable, high-performance time-series database.
- **Grafana**: Visualizes the collected data with custom dashboards.

## Prerequisites

Before you begin, ensure you have the following tools installed on your machine:
- **Containerization Tools**: [Docker](https://docs.docker.com/engine/install/) and [Docker Compose](https://docs.docker.com/compose/install). We'll use several docker compose feature, so better check this [docs](https://docs.docker.com/compose/) too.
- **Development Tools**: [Git](https://git-scm.com/downloads) for version control and [Visual Studio Code](https://code.visualstudio.com/download) for editing source code and configuration files.
- **Time and Motivation**: Setting up monitoring can be rewarding for troubleshooting and analyzing your system's performance.

## Installation



Clone this repository to your local machine:

```bash
git clone https://github.com/your-username/simple-monitoring.git
cd simple-monitoring
```

## Usage

Once the stack is up and running, you can:

View Metrics: Open Grafana in your browser to view system and container metrics.
Customize: Tailor the dashboards to monitor the metrics you care about most.
To stop the monitoring stack, use:
```bash
git clone https://github.com/your-username/simple-monitoring.git
cd simple-monitoring
```

## Configuration

### Environment Variables
Adjust the environment variables to suit your needs. Environment variables can be defined in a .env file in the project root, which Docker Compose will automatically load.

### Configuring Telegraf
Modify the telegraf.conf file to adjust the metrics collection to your requirements (e.g., CPU, memory, disk usage, etc.).

### Grafana Dashboards
Grafana is accessible at http://localhost:3000.
The default login credentials are:
Username: admin
Password: admin
You can import pre-configured dashboards or create custom ones based on your monitoring needs.


## Reference

This project is inspired by [san-gg's telegraf-prometheus-grafana](https://github.com/san-gg/telegraf-prometheus-grafana) repository, with adjustments to suit specific use cases. Check out his repository for more inspiring projects.
Credits goes to **san-gg**, I'm inspired by his [san-gg/telegraf-prometheus-grafana]() projects and did a bit of adjustment to my needs. You should checkout his repo for other amazing projects.


## License 

[Apache 2.0](LICENSE)


