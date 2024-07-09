### What is Prometheus?
Prometheus is an open-source tool used in DevOps for monitoring and alerting. It tracks the performance and health of applications and infrastructure, making it essential for maintaining reliable and efficient systems.

⭐ Key Features:
1. Time Series Data: Prometheus stores data with timestamps, making it easy to track changes over time.
2. Query Language (PromQL): This allows users to fetch and analyze metrics.
3. Standalone Server: Prometheus works independently, storing its data locally for reliability.
4. Pull-Based Collection: It collects metrics by pulling them from specified endpoints.
5. Alerting and Visualization: Prometheus can send alerts and visualize data using tools like Grafana.

It integrates well with visualization tools like Grafana, providing clear and customizable dashboards. For alerting, Prometheus works with Alertmanager to send notifications based on defined conditions, helping teams respond to potential issues promptly.

### What are Exporters in Prometheus?
Exporters are tools that collect data (metrics) from various sources (like servers, databases, applications) and make it available for Prometheus to gather and monitor.

### What is a Node Exporter
Purpose: Collects hardware and OS metrics from Linux/Unix systems.
Metrics: CPU, memory, disk, and network usage.
Use Case: Monitoring servers.

### How to setup Node Exporter
Download and Extract the tar file and run it using the below command

💎 ./node_exporter

Configure Prometheus to Scrape Node Exporter by adding the below configuration to the 'prometheus.yml' file.

         scrape_configs:
          -job_name:'node'
          static_configs:
          - targets: ['localhost:9100']

Exporters help Prometheus gather data from different systems and services, making it easier to monitor everything in one place.

### What is Grafana? 
Grafana is an open-source tool used for analytics and monitoring. It stands out for its ability to connect with any data source like Prometheus, MySQL and Elasticsearch etc. This flexibility allows users to build complete dashboards for a holistic view of your operational metrics.

### What are the uses of Grafana:
1. Track your system's health, performance metrics, and usage patterns as they happen.
2. With many visualization options including graphs, charts, maps and alerts, Grafana is facilitating the understanding of complex data.
3. Create alerts that automatically notify you at the first sign of trouble, 24/7.

### How Does Grafana Work?
Connect Data Sources: Grafana lets you pull data from various sources. Whether it's time-series databases, SQL databases, or even cloud services, Grafana integrates seamlessly.

Create Dashboards: Utilize Grafana's intuitive UI to craft dashboards that highlight the metrics most important to you. Customize and explore data through graphs, charts, and tables.


