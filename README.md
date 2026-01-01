# Double-Server Call Center Simulation Analysis

#📌 Project Overview

This project provides a Python-based simulation of a technical support call center using a Double-Server Queuing Model. It specifically implements the classic "Able & Baker" scenario to analyze how prioritizing service personnel with different skill levels affects overall system efficiency and customer satisfaction.

The simulation models 70,000 unique customer interactions (700 customers across 100 trials) to ensure high statistical reliability.

#⚙️ System Configuration

The system operates with a stochastic arrival process and two servers with distinct performance profiles:

Arrival Process: Exponential distribution with a Mean Inter-arrival Time of 4.0 minutes.

Operating Hours: Starts at 9:00 AM.

Service Personnel:

Able (Expert): Prioritized technician, Mean service time = 3.0 minutes.

Baker (Trainee): Secondary technician, Mean service time = 0.9 minutes.

#🧠 Simulation Logic

The core of this project is the Rule-Based Assignment System:

Priority 1: If Able is idle, assign the customer to Able.

Priority 2: If Able is busy but Baker is idle, assign the customer to Baker.

Queue: If both servers are busy, the customer joins a queue and waits for the first available technician.

Tie-Break: If both finish simultaneously, Able is assigned.

#📊 Key Results

Based on the 100-trial simulation, the system demonstrates high stability:

Average Waiting Time: ~0.07 minutes.

Probability of Waiting: ~8%.

Server Idle Probability: ~73% (indicating high scalability).

Average System Time: ~2.19 minutes.
