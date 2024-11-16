
# The Three Context Framework

**Principles for Building Resilient Cloud-Native Applications**

---

## 1. Self-Healing

**Recover from internal and external faults autonomously.**

- Detect anomalies: Use health checks and monitoring tools.
- Retry intelligently: Employ retry mechanisms with exponential backoff.
- Isolate faults: Apply circuit breakers to avoid cascading failures.

**Example:**  
A service using Kubernetes health probes detects a crash and restarts the affected container without disrupting the user experience.

---

## 2. Remote Connection Self-Management

**Adapt to dynamic environments by connecting, reconnecting, and supervising external systems.**

- Monitor and supervise remote dependencies continuously.
- Use dynamic connection handling (e.g., service discovery and DNS updates).
- Fall back to cached data or degraded modes when external systems fail.

**Example:**  
An API client automatically switches to a backup endpoint during an outage without user intervention.

---

## 3. Resource and Scaling Management

**Prevent system overload by managing contention, rate limits, and graceful degradation.**

- Implement rate limiting to control incoming traffic.
- Use backpressure techniques to handle surges.
- Scale resources dynamically (vertically or horizontally) based on demand.

**Example:**  
An API Gateway throttles incoming requests when the backend reaches maximum memory usage, preventing system crashes.

---

**Started at [scanales.com](https://scanales.com)**
