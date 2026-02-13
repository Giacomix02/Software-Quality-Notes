# Software Performance - Notes

## Basic Units

- **Observation Time ($T$)**

    - The total duration of time during which the system or resource was monitored
- **Number of arrivals ($A$)**
    - The total count of requests or tasks that entered the system during the **Observation Time** 
- **Number of completitions ($C$)**
    - The total count of requests or tasks that successfully finished processing during the **Observation Time**
- **Busy time ($B$)**
    - The cumulative amount of time during the **Observation Time** ($T$) that the resource was actually processing requests
- **Accomulated time ($W$)**
    - number of total time (???)

## Metrics Definitions and formulas

- **Arrival Rate ($\lambda$)**
    - The frequency at which new requests or tasks enter the system over a specific period
    - $\lambda = A/T$

- **Service Time ($S$)**
    - The actual time a resource (like a CPU) spends processing a specific request
    - $S = B/C$

- **Service Rate ($\mu$)** 
    - Frequency at which a system processes requests
    - $\mu = 1/S$

- **Utilization Time ($U$)**
    - The fraction or percentage of time that a resource is busy processing requests
    - $U = \frac{B}{T} \quad$ dove $\quad 0 \le U \le 1$

- **Throughput ($X$)**
    - The rate at which requests are successfully completed and delivered by the system
    - $X = \frac{C}{T}$

- **Avarage Response Time ($R$)**
    - The average amount of time a single job spends in the system from arrival to completion.
    - $R = W/C$

- **Avarage Numbers of Jobs ($N$)**
    - The average number of requests present in the system (either waiting or being processed) during the observation interval
    - $N = W/T$

## Laws
- **Utilization Law**
- **Little's Law**
- **Forced Flow Law**



[Return Index](./README.md)