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
    - The total **cumulative time** spent by all jobs (requests) within the system during the observation period.

## Metrics Definitions and formulas

- **Arrival Rate ($\lambda$)**
    - The frequency at which new requests or tasks enter the system over a specific period
    - $\lambda = \frac{A}{T}$

- **Service Time ($S$)**
    - The actual time a resource (like a CPU) spends processing a specific request
    - $S = \frac{B}{C}$

- **Service Rate ($\mu$)** 
    - Frequency at which a system processes requests
    - $\mu = \frac{1}{S}$

- **Utilization Time ($U$)**
    - The fraction or percentage of time that a resource is busy processing requests
    - $U = \frac{B}{T} \quad$ where $\quad 0 \le U \le 1$

- **Throughput ($X$)**
    - The rate at which requests are successfully completed and delivered by the system
    - $X = \frac{C}{T}$

- **Avarage Response Time ($R$)**
    - The average amount of time a single job spends in the system from arrival to completion.
    - $R = \frac{W}{C}$

- **Avarage Numbers of Jobs ($N$)**
    - The average number of requests present in the system (either waiting or being processed) during the observation interval
    - $N = \frac{W}{T}$ 

## Laws
- **Utilization Law** ($U = X \cdot S$)

    - Calculate the **Utilization Time ($U$)** from **Throughput ($X$)** and **Service Time ($S$)**
    - $U = X \cdot S \quad$ where $\quad 0 \le X \cdot S \le 1 \quad$ and having $\quad X \le \frac{1}{S} \quad$ and the $\quad \mu \quad$ formula, we can say that ***$\quad X \le \mu$***

- **Little's Law** ($N = X \cdot R$)
    - Calculate the **Avarage Numbers of Jobs ($N$)** from:
        - Throughput ($X$)
        - Avarage Response Time ($R$)
    - **How the formula come from?** Having:
        - $\frac{W}{T}$ is the Average Number of Jobs ($N$) in the system.
        - $\frac{C}{T}$ is the Throughput ($X$).
        - $\frac{W}{C}$ is the Average Response Time ($R$).
        - And simply do: $\frac{W}{T} = \frac{C}{T} \times \frac{W}{C}$
    - From this law we can also calculate an other relation about the **Avarage Response Time ($R$)**
        - $R = N \cdot \frac{1}{X}$
        
## Single node Laws and relations (Open System)

- **Completions in time $T$** ($C$)
    - Number of job completed in a defined time in **all system**
    - $C_{D1}$ mean the number of job completed for **single ($D1$) processor**

- **Number of Visits** ($V_i$)
    - average number of times a single job requests service from a specific resource $i$ during its stay in the system
    - $V_i = \frac{C_i}{C}$

- **Demand** ($D_i$)
    - total time spent on average in the i-th node
    - $D_i = V_i \cdot S_i$

### Laws

- **Forced flow law** ($X_i = V_i \cdot X$)
    - describes the **relationship** between the *Throughput* of a ***single component*** and the *total Throughput* of the **entire system**

- **Utilization Law for** *single node*($U_i = X \cdot D_i$)

#### Little's Law

- **Little's Law for** *single node* ($N_i = X_i \cdot $) 

- **Little's Law for** *entire system* ($R = \sum_i \frac{N_i}{X}$)

From this two relations we can obtain a new relation about the **Avarage response time**:
$$R=\sum_i V_i \cdot R_i$$

 ### Relations with demand

 We want to maximaze the **Demand** $D$

 $$D_{max}=max\{V_i ; S_i\}$$

 From the little low we also have:
 $$X \le \frac{1}{D_{max}}$$
 From the Little law: 
 $$N = X \cdot R\quad so \quad R=\frac{N}{X}$$
 **Finally** we have:
 $$R \ge N \cdot D_ {max}$$




[Return Index](./README.md)