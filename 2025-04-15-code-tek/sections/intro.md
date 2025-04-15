---
layout: default
---

<h1 class="text-blue-500 font-bold pb-4">Key Topics</h1>

- What is observability and why should we observe our application?

- What to observe from a system? Golden signals and its role in site reliability engineering.

- The three main pillars of application observability, metrics, logs, and traces

- Grafana LGTM stack (Loki, Grafana, Tempo and Mimir)

- Building visualisation applications

---
layout: default
---

<h1 class="text-blue-500 font-bold pb-4">What is observability and why should we observe our application?
</h1>

# Monitoring

# Observable

# Observability

---
layout: default
---

<h1 class="text-blue-500 font-bold pb-4">Monitoring
</h1>

- Monitoring is the **process** of collecting, analyzing, and displaying predefined metrics to track the health and performance of systems. Monitoring is a subset of observability.
<h4 class="text-blue-500 font-bold py-4">Goal
</h4>
 To detect known problems and alert when something goes wrong

<h4 class="text-blue-500 font-bold py-4">Examples
</h4>

- CPU usage over 80%? 🔔 Alert!
- HTTP 500 errors increased? 🚨 Something’s off!

<h4 class="text-blue-500 font-bold py-4">Focus
</h4>
Dashboards, Alerts , Thresholds
---
layout: cover
---

What is an observable system?

<h2 class="!text-blue-500 font-bold pb-4">A system is observable if you can determine its internal state based on external outputs.
</h2>

---
layout: default
---

<h1 class="text-blue-500 font-bold pb-4">Observability
</h1>

- Observability is the ability to understand what’s happening inside a system just by looking at what it outputs—like logs, metrics, and traces

<h4 class="text-blue-500 font-bold py-4">Goal
</h4>
 To help you explore unknown problems—especially complex  failures.

<h4 class="text-blue-500 font-bold py-4">Examples
</h4>

- "Why did this request fail even though the CPU is fine?"
- “Why did this request take longer than usual?”

<h4 class="text-blue-500 font-bold py-4">Focus
</h4>
Logs 📜
Metrics 📊
Traces 🔁
Ad-hoc debugging 🛠️

---
layout: default
---

<h1 class="text-blue-500 font-bold pb-4">How Monitoring and Observability Are Connected
</h1>

- Think of observability as the whole toolbox, while monitoring is one specific tool inside it.

<h4 class="text-blue-500 font-bold py-4">Can you have observability without monitoring?
</h4>

<h4 class="text-blue-500 font-bold py-4"> Can you have monitoring without observability?
</h4>


- Monitoring without observability is like,
you know the alarm is ringing, but you have no idea what room it’s coming from or why.

---

<h1 class="text-blue-500 font-bold pb-4">What to observe from a system? Golden signals and its role in site reliability engineering.
</h1>

1. **Latency**
    - How long does it take to serve a request?
2. **Traffic**
    - How much demand is being placed on the system?
3. **Errors**
   - How often does the system fail to do what’s expected?
4. **Saturation**
   - How full is your system?


---

<h1 class="text-blue-500 font-bold pb-4">Why the Golden Signals Are Important
</h1>

- **Quick diagnosis**: Helps detect most common issues fast.

- **SLO-friendly**: They align well with Service Level Objectives (SLOs)

- **Universal**: These apply across systems, from APIs to queues to databases.


---

<h1 class="text-blue-500 font-bold pb-4">Example: A Real-Life Incident
</h1>

Your app slows down. You check:

- Latency: requests are taking 5x longer

- Traffic: normal

- Errors: increased 500s

- Saturation: CPU is at 95%

--> You’ve quickly narrowed the cause to resource exhaustion

---
layout: default
---

<h1 class="text-blue-500 font-bold pb-4">The three main pillars of application observability, metrics, logs, and traces
</h1>



| Pillar   | What It Is                             | Purpose                              | Example                                   | Strengths                              |
|----------|----------------------------------------|---------------------------------------|-------------------------------------------|----------------------------------------|
| 📊 Metrics | Numeric data measured over time        | Detect system health & trends         | `CPU Usage = 85%`, `500 errors/min`       | Lightweight, good for alerts & dashboards |
| 📜    Logs    | Time-stamped text records of events    | Describe what happened & when         | `User login failed`, `DB timeout error`   | High detail, great for debugging       |
| 🔍 Traces  | End-to-end view of a request's journey | Understand flow across services       | `Trace ID abc123 took 2.3s in total`      | Shows bottlenecks & dependencies       |

