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

## System Performance vs Software Performance

### System Performance

- *Indices* refer to **actual time measures** under certain workloads
- **System** may be a **generic term** (e.g. a device, a PC, etc.)

### Software Performance

- *Indices* may refer to **actual time measures** (software+platform models) or to **parametric descriptions** (software models)
- In order to **synthesize** the workload the **software must be explicitly modeled**

- **Goal:**
    - find **bottlenecks** also at the software level


## Performance Engineering

### During Architectural Design

-  Set Explicit **Performance Goals**
- Work with **customer**(s) to understand **workload & application**
- Build initial model(s)
- Find performance **bottlenecks in the software**
- Evaluate *sizing* (**how much hardware**) and fattibility
- Compare **alternative architectures**

### During Testing
- **Debug/validate models** & testbed
-  **Measure performance of components** and subsystems
- **Verify** that performance **goals have been met**
    - work with developers to **resolve any performance shortfalls**
- Use profiling tools to characterize products

### After Deployment
- Present/publish measurement results
- Present/publish tuning recommendations for configurable products
- **Collect measurements at customer sites**
-  Work with developers and support organization to resolve performance problems that arise in the field
- Suggest **enhancements** for **future versions** of product



[Return Index](./README.md)