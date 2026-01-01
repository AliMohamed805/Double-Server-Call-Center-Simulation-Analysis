# Double-Server Queuing Simulation 

## 📌 Overview
This project implements a **Python-based discrete-event simulation** of a technical support call center using a **double-server queuing system**, commonly known as the **Able & Baker model** in Operations Research.

The simulation analyzes how **priority-based server assignment** with heterogeneous service rates impacts:
- Customer waiting time
- Probability of delay
- Server utilization
- Overall system efficiency

To ensure statistical reliability, the system simulates **70,000 customer interactions** (700 customers × 100 independent trials).

---

## ⚙️ System Configuration

### Arrival Process
- **Distribution:** Exponential (Poisson arrivals)
- **Mean inter-arrival time:** 4.0 minutes
- **Operating start time:** 9:00 AM

### Service Personnel
| Server | Role | Priority | Mean Service Time |
|------|------|---------|------------------|
| Able | Expert Technician | High | 3.0 minutes |
| Baker | Trainee Technician | Low | 0.9 minutes |

---

## 🧠 Simulation Logic

Customer assignment follows a **rule-based priority system**:

1. If **Able is idle**, assign the customer to Able.
2. If Able is busy and **Baker is idle**, assign the customer to Baker.
3. If both servers are busy, the customer **joins a queue**.
4. When both servers finish simultaneously, **Able is selected** (tie-break rule).

This logic reflects real-world call center prioritization where expert staff are preferred when available.

---

## 📊 Key Results (100-Trial Average)

| Metric | Value |
|------|------|
| Average Waiting Time | ~0.07 minutes |
| Probability of Waiting | ~8% |
| Average Time in System | ~2.20 minutes |
| Server Idle Probability | ~19% |

These results indicate:
- Very low congestion
- High scalability
- Efficient prioritization strategy

---

## 📈 Visualizations

The simulation generates **histograms of total time in system**, showing that:
- Most customers experience zero waiting.
- Delays are rare and short.
- Priority assignment significantly improves service performance.
