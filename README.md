<p align="center">
  <img src="docs/logo_behavload.png" alt="behavload" width="150"/>

<h1 align="center">BehavLoad</h1>

<h3 align="center">Advanced Behavioral Load Testing Engine</h3>

[![Linux](https://img.shields.io/badge/Linux-Compatible-black?style=for-the-badge\&logo=linux\&logoColor=white)]()
[![Go](https://img.shields.io/badge/Go-Engine-00ADD8?style=for-the-badge\&logo=go\&logoColor=white)]()
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](./LICENSE)
[![Status](https://img.shields.io/badge/Status-Em%20Desenvolvimento-yellow?style=for-the-badge)]()

> **Simulate users. Not requests.**
> Move beyond naive load testing by modeling real user behavior using probabilistic state machines and decision trees.

</p>
</div>

---

## 📋 Index

* [About the Project](#-about-the-project)
* [Features](#-features)
* [Architecture & Technologies](#-architecture--technologies)
* [Prerequisites](#-prerequisites)
* [Installation](#-installation)
* [How to Use](#-how-to-use)
* [User Profiles](#-user-profiles)
* [Roadmap](#-roadmap)
* [Contributing](#-contributing)
* [License](#-license)

---

## 🎯 About the Project

**BehavLoad** is a high-performance load testing engine designed to simulate **realistic user behavior at scale**.

Instead of generating static or repetitive HTTP requests, BehavLoad models each virtual user as an independent agent driven by **probabilistic state machines or decision trees**, enabling dynamic, adaptive, and context-aware interactions.

### The problem we solve

| Traditional Load Testing | BehavLoad                |
| ------------------------ | ------------------------ |
| Static request patterns  | Behavioral simulation    |
| Unrealistic traffic      | Realistic user flows     |
| Fixed scripts            | Adaptive decision models |
| No context awareness     | Session-aware execution  |

---

## ✨ Features

### 🧠 1. Behavioral Simulation Engine

> *Core Differentiator — the intelligence layer*

Each virtual user behaves like a real user:

* State machines / decision trees
* Probabilistic transitions
* Context-aware decisions
* Response-driven behavior

---

### ⚡ 2. High-Concurrency Execution

* Event-driven architecture (no thread-per-user)
* Thousands of users per worker
* Low memory footprint
* Optimized for Linux environments

---

### 🌐 3. Distributed Load Orchestration

* Coordinator + Workers model
* Horizontal scalability
* Dynamic load distribution

---

### ⏱ 4. Realistic Timing Simulation

* Think time modeling
* Session persistence
* User abandonment logic *(planned)*

---

### 📊 5. Observability & Metrics *(Planned)*

* Latency (p50, p95, p99)
* Throughput
* Error rates
* Behavior-level analytics

---

## 🏗️ Architecture & Technologies

> *Designed for performance, scalability and realism.*

### System Overview

```
Coordinator (Control Plane)
    ├── Scenario Management
    ├── Load Distribution
    └── Metrics Aggregation

Workers (Data Plane)
    ├── Event Loop Engine
    ├── Virtual Users Simulation
    └── Metrics Reporting
```

---

### Suggested Stack

```
🧠 Core Engine
├── Go (Golang)
├── Goroutines (lightweight concurrency)
├── Async I/O

🔗 Communication
├── gRPC / NATS

📊 Observability
├── Prometheus
├── Grafana

⚙️ Config
├── YAML / JSON
```

---

## 📦 Prerequisites

Before running or contributing:

* **OS:**

  * Linux (recommended)

* **Development:**

  * Go `1.20+`

* **Optional:**

  * Docker
  * Prometheus + Grafana

---

## 🚀 Installation

### Option A — Local Development

```bash
git clone https://github.com/your-username/behavload.git
cd behavload

go mod tidy
go run ./cmd/main.go
```

---

### Option B — Docker *(planned)*

```bash
docker build -t behavload .
docker run behavload
```

---

## 🧭 How to Use

### 1. Define a Scenario

Create a behavior model:

```
Login → Browse → Action → Exit
```

With probabilities:

* Retry login: 20%
* Abandon session: 10%

---

### 2. Run Simulation

* Configure number of users
* Define workers
* Execute load

---

### 3. Analyze Results

* Observe latency
* Identify bottlenecks
* Evaluate system resilience

---

## 👥 User Profiles

### 👨‍💻 Backend Engineer

Stress test APIs with realistic traffic patterns.

### 🧪 QA Engineer

Validate system behavior under dynamic user flows.

### ⚙️ SRE / DevOps

Simulate production-like scenarios before deployment.

---

## 🗺️ Roadmap

```
v0.1 — Core Engine

✅ Basic worker
✅ State machine execution
✅ HTTP simulation

v0.2 — Behavior Layer

🔲 Decision trees
🔲 Probabilistic transitions
🔲 Think time

v0.3 — Distributed System

🔲 Multi-worker orchestration
🔲 gRPC communication
🔲 Metrics aggregation

v0.4 — Observability

🔲 Prometheus integration
🔲 Dashboards
🔲 Behavior analytics

v1.0 — Production Ready

🔲 CLI interface
🔲 Scenario configuration
🔲 Documentation
```

---

## 🤝 Contributing

To contribute:

1. Fork the repository
2. Create a branch (`feature/your-feature`)
3. Commit your changes
4. Push and open a Pull Request

---

## 📄 License

This project is licensed under the **MIT License**.

---

<div align="center">

Built for engineers who test reality, not assumptions.

</div>
