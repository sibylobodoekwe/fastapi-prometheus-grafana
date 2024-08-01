<h1 align="center">FastAPI + Prometheus + Grafana + Loki + CheckMK + Traefik + Metabase :tada:</h1>

This repository provides a comprehensive setup for monitoring a FastAPI microservice, incorporating a variety of monitoring and observability tools.

## Overview

This setup includes the following components:

- **FastAPI**: The microservice you're monitoring.
- **Prometheus**: For metrics collection and querying.
- **Grafana**: For visualizing metrics from Prometheus.
- **Loki**: For logging and log aggregation.
- **Check_MK**: For comprehensive monitoring and alerting.
- **Traefik**: For dynamic reverse proxy and load balancing.
- **Metabase**: For interactive data exploration and analytics.

## Installation

Ensure you have the following prerequisites installed:

* [Docker](https://docs.docker.com/get-docker/)
* [Docker Compose](https://docs.docker.com/compose/install/)

Clone the repository:

```bash
git clone https://github.com/sibylobodoekwe/fastapi-prometheus-grafana-loki-checkmk-traefik
cd fastapi-prometheus-grafana-loki-checkmk-traefik
```

## Usage

Start the Docker containers with the following command:

```bash
docker-compose up -d --build
```

After running the above command, you'll have access to the following services and their respective ports:

* **Prometheus**: [http://localhost:9090/](http://localhost:9090/)
* **Grafana**: [http://localhost:3000/](http://localhost:3000/)
* **FastAPI**: [http://localhost:8000/](http://localhost:8000/)
* **Loki**: [http://localhost:3100/](http://localhost:3100/)
* **Check_MK**: [http://localhost:8081/](http://localhost:8081/)
* **Metabase**: [http://localhost:3001/](http://localhost:3001/)
* **Traefik Dashboard**: [http://localhost:8080/](http://localhost:443/)

### Metrics and Logging

- **FastAPI Metrics**: Access the `/metrics` endpoint of your FastAPI application to see the metrics Prometheus is scraping.
- **Logs**: View and analyze logs through Loki.
- **Monitoring and Alerts**: Configure and monitor various metrics and alerts with Check_MK.

## Configuration

- **Prometheus**: Metrics scraping configuration is located in `./prometheus/prometheus.yml`.
- **Grafana**: Dashboard provisioning is configured in `./grafana/provisioning`.
- **Loki**: Configuration file is at `./loki/loki-config.yml`.
- **Check_MK**: Monitoring configuration is in `./check-mk/checkmk.yml`.
- **Traefik**: Traefik's configuration is in `./traefik/traefik.yml`.
- **Metabase**: Metabase configuration files are located in `./metabase`.

## How It Looks Like

<p align="center">
  <img src="./dashboard.jpeg" alt="Dashboard Screenshot">
</p>

## References

* [Prometheus FastAPI Instrumentator](https://github.com/trallnag/prometheus-fastapi-instrumentator)
* [Generate and Track Metrics for Flask API Applications Using Prometheus and Grafana](https://medium.com/swlh/generate-and-track-metrics-for-flask-api-applications-using-prometheus-and-grafana-55ddd39866f0)
* [PromQL for Humans](https://timber.io/blog/promql-for-humans/)
* [Loki Documentation](https://grafana.com/docs/loki/latest/)
* [Check_MK Documentation](https://docs.checkmk.com/latest/en/)
* [Traefik Documentation](https://doc.traefik.io/traefik/)
* [Metabase Documentation](https://www.metabase.com/docs/latest/)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
```