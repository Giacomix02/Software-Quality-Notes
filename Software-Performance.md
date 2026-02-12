# Introduction to Software Performance

## What is Performance Analysis?
The science of quantitatively **measuring**, **understanding**, and **predicting** performance **indices** of computer systems

- **Latency (or Response Time)**: Delay between start and end of an operation (*or between request and response*)
- **Throughput**:  work completed per unit time (*messages/second*, *transactions/minute*)
- **Utilization**:  Fraction of time a resource (CPU, disk, network, software component) is busy

### Analytic Modeling vs Simulation Models

#### Analytic Modeling

- **Advantages** of *Analytic Models*
    - Provide **quick answers** since they are easy to construct
    - Rapid evaluation
    - **Easy to refine** as more information becomes available
-  **Disadvantages** of Analytic Models
    - Need to make **simplifying assumptions**
    - It’s easy for skeptics to **question assumptions & model**

#### Simulation Models

Identify **key resources** and **events** in a system, then write (simulation) software to a workload that models how the system responds. The model must describe timing accurately

- Three key aspects:
    - Level of **detail**
    - **Simulation paradigm**: event-driven or time-driven
    - **Workload** selection and representation

## Inputs and outputs of a Performance Model

- Inputs:
    - **Workload**: Number of requests per unit of time
    - **Operational Profile**: Probability of execution of “some part” of the software

- Outputs:
    - **Service Demands**: Amount of resources needed to execute “some part” of the software
    - **Service Rate**: Number of operations of a device per unit of time

## 

[Return Index](./README.md)