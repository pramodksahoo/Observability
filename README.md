# Introduction to Observability

**Observability** is the ability to understand the internal state of a system by analyzing the data it produces, including logs, metrics, and traces.

## Core Pillars of Observability

### 🔍 Monitoring (Metrics)
- Tracks system metrics like CPU usage, memory usage, and network performance.
- Provides alerts based on predefined thresholds.
- **Purpose**: Tells us _what_ is happening.

### 📜 Logging (Logs)
- Collects log data from various system components.
- **Purpose**: Explains _why_ something is happening.

### � Tracing (Traces)
- Tracks the flow of a request/transaction across services and components.
- **Purpose**: Shows _how_ it is happening.

![architecture](https://github.com/user-attachments/assets/1ff3470d-bb61-4ed6-bd3a-f4bc1baba881)

---

## Monitoring vs. Observability: Key Differences

| **Category**       | **Monitoring**                                      | **Observability**                                   |
|---------------------|-----------------------------------------------------|-----------------------------------------------------|
| **Focus**           | Checks if the system works as expected              | Understands why things happen                      |
| **Data**            | Metrics (CPU, memory, error rates)                  | Logs, metrics, traces                              |
| **Alerts**          | Sends notifications for issues                     | Correlates events to identify root causes          |
| **Example**         | Alert on server CPU > 90%                           | Trace a slow user request to find bottlenecks      |
| **Insight**         | Identifies potential issues early                  | Diagnoses issues and explains system behavior       |

> 🔥 **Monitoring** answers the *when* and *what*; **Observability** answers the *why* and *how*.

---

## 🔭 Does Observability Cover Monitoring?
**Yes!** Monitoring is a subset of Observability.  
- **Monitoring**: Tracks metrics and alerts on predefined conditions.  
- **Observability**: Provides a comprehensive view using logs, metrics, and traces.

---

## 🖥️ What Can Be Monitored?
- **Infrastructure**: CPU, memory, disk I/O, network traffic.
- **Applications**: Response times, error rates, throughput.
- **Databases**: Query performance, connection pools, transactions.
- **Network**: Latency, packet loss, bandwidth.
- **Security**: Unauthorized access attempts, firewall logs.

---

## 👀 What Can Be Observed?
- **Logs**: Detailed event/transaction records.
- **Metrics**: Quantitative data (CPU load, request counts).
- **Traces**: Request flow across services.

---

## ⚒️ What are the Tools Available?

### Monitoring Tools
- Prometheus, Grafana, Nagios, Zabbix, PRTG.

### Observability Tools
- **Logs**: ELK Stack (Elasticsearch, Logstash, Kibana), EFK Stack (Elasticsearch, FluentBit, Kibana), Splunk.
- **Traces**: Jaeger, Zipkin, New Relic, Dynatrace, Datadog.


---

## Why Fluent Bit or Promtail?

**Fluent Bit** is a lightweight log processor/forwarder for Kubernetes, used to collect, parse, and ship logs to destinations like Elasticsearch or Loki.

### Comparison of Logging Tools

| **Feature**           | Fluent Bit | Fluentd | Logstash | Promtail | Vector |
|-----------------------|------------|---------|----------|----------|--------|
| **Lightweight**       | ✅         | ❌      | ❌       | ✅       | ✅     |
| **Ease of Config**    | ✅         | ✅      | ❌       | ✅       | ✅     |
| **K8s Metadata**      | ✅         | ✅      | ❌       | ✅       | ✅     |
| **Performance**       | ✅         | ❌      | ❌       | ✅       | ✅     |
| **Versatility**       | ✅         | ✅      | ✅       | ❌       | ✅     |

---

## 🎛️ Instrumentation
**Instrumentation** adds monitoring capabilities to applications by embedding code or using tools to collect metrics, logs, and traces.

### 🎯 Purpose
- **Visibility**: Understand internal application/infrastructure state.
- **Metrics**: Track health/performance (CPU, errors, request rates).
- **Troubleshooting**: Diagnose issues quickly.

### ⚙️ How It Works
- **Code-Level**: Add libraries (e.g., `prom-client` for Node.js) to expose metrics.
- **OpenTelemetry**: Use language-specific libraries (e.g., PHP zero-code instrumentation).

---

> 📘 **Next Steps**: Follow the linked guides to onboard to our Observability platform.
