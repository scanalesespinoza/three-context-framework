
# The Three Context Framework

**Principles for Building Resilient Cloud-Native Applications**

## Introduction

After a decade of Kubernetes, the cloud has become the foundation of modern computing. This massive adoption has brought rapid changes, continuous evolution, and a surge in derived technologies. While these innovations have accelerated progress, they have also made it increasingly challenging to ensure the quality of workloads and business services. The rapid growth of solutions and technologies often outpaces people's ability to learn and adapt, creating a knowledge gap.

As a result, baseline design and development for the vast majority of applications often lack the necessary quality. Instead, they rely heavily on external capabilities, such as functional add-ons using sidecar patterns, intermediary services, or platforms. This approach adds multiple layers of abstraction that ideally would be intrinsic to the business component itself.

There has also been a significant misunderstanding surrounding concepts like "enabling developers to focus on business value" or the use of low-code/no-code frameworks. While both aim to maximize developer productivity, they should never come at the cost of quality or reliability. Striking a balance between leveraging advanced technologies and maintaining essential knowledge and experience is critical—not necessarily for day-to-day operations, but especially when addressing complex problems rooted in the accumulation of technical debt across multiple layers.

With the added impact of AI-driven changes, it is imperative to revisit fundamental principles. By focusing on the essential behaviors and capabilities of applications, we can build robust and responsible business services that thrive across the cloud.

To dive deeper into this approach, explore the Three Context Framework for Building Resilient Cloud-Native Applications, a methodology designed to ensure reliability, quality, and long-term success in the cloud.
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

**The principles are inspired by a lifetime delivering application/services and lately Cloud Native success, demands and pitfalls.**
