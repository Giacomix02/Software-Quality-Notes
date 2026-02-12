# Software Reliability and similar quality attributes

## Reliability definition
- `The ability of an item to perform a required function under given conditions for a givrn time interval`
- `Probability of a system working withon specs throughtput an interval of time without system-level repair`
    - if there is also a certain number of invocations this is called **Reliability on demand**

## Faults, Errors and Failures

- **Fault**: feature that precludes the software from operating according to its specifications
    - *Fault* do not necessary reslt in system errors because the sistem never execute the faulty statement
- **Error**:  the value of the software state differs from the expected one
    - *Error* don't necessarily lead to system failures thanks to **built-in error detection and recovery** or masked from other components
- **Faliure**: the actual software output (for some input) differs from the expected one
    - a *Faliure* is usually a result of a system error that is derived from *Fault* in the system

### How to avoid Faults

- **Fault avoidance**
    - Devlop techniques that **minimize the possibility of mistakes** or trap mistakes before they cause a Fault
- **Fault detection and removal**
    - detecting and correcting Faults before the system goes into service
- **Fault tolerance**
    - Run-time techniques are used to ensure that system Faults **do not result in system errors** and/or that system Errors do not lead to system Failures

## Fault classification
- Permanent (needs repair or replacements)
- Intermittent (reboot/restart)
- Transient (rety)
- Design:
    - Mandelbugs
    - Bohrbugs
    - Heisenbugs

### Bohrbugs
Is a **repetable bug**, that is manifested under a possibly unknown but well-defined set of conditions.

Many software bugs are **easy to find and resolve** during testing and debugging

### Heisenbugs
A bug that **disappears** or **alters its behavio**r when one attempts to probe or isolate it. 

>E.g., the use of a debugger sometimes alters a program's operating environment significantly enough that buggy code, such as that which relies on the values of uninitialized memory, behaves quite differently.

### Mandelbugs 
A bug whose underlying causes are so complex and obscure as to make its **behavior appear chaotic or even non deterministic**

## Failure classification

### Nature of the Failure

- *Hardware Failure*
    - caused by design and manufacturing errors or because components have reached the end of their natural life

- *Software Faliure*
    - errors in its specification, design or implementation
    - A difference from *Hardware Failure* is that the software can continue in operation even after an incorrect result has been produced

- *Operational Faliure*
    - Human operatator: perhaps the largest single cause of system failures


### Type of Failure

- *Omission failures* (send or recive failures)
    - Crash
    - infinite loop
- *Timing failures*
    - Early
    - Late (performance or Dynamic failures)
- *Response failures*
    - Value failures
    - State-transition failures




### Severity of Failure

| **Failure class** | Description |
| :--- | :--- |
| **Transient** | Occurs only with certain inputs |
| **Permanent** | Occurs with all inputs |
| --- | --- |
| **Recoverable** | System can recover without operator intervention |
| **Unrecoverable** | Operator intervention needed to recover from failure |
| --- |---|
| **Non-corrupting** | Failure does not corrupt system state or data |
| **Corrupting** | Failure corrupts system state or data |


## Reliability improvement

-  **Removing X% of the faults** in a system **will not** necessarily **improve the reliability** by X%
- Program defects **may be in rarely executed sections** of the code so may never be encountered by users
    - Removing these does not affect the perceived reliability
- A program with known faults ***may be*** seen as reliable by its users


## Reliability specifications
- The required **level of system reliability** should be expressed **quantitatively**
- **Reliability** is a **dynamic system** attribute 
    - reliability specifications  related to the source code are meaningless
- An **appropriate reliability metric** should be chosen to specify the overall system reliability

## Reliability assessment problems
- **Operational profile uncertainty**
    - The operational profile may not be an accurate reflection of the real use of the system
- **High costs of test data generation**
    - Costs can be very high if the test data for the system cannot be generated automatically
- **System observation can be intrusive**
    - The observer may change the expected results
- **Statistical uncertainty**
    - You need a statistically significant number of failures to compute the reliability but highly reliable systems will rarely fail

## Reliability metrics

Reliability metrics are **units of measurement** of system reliability

System **reliability** is measured by **counting the number of operational failures** and, where appropriate, relating these to the demands made on the system and the time that the system has been operational

### POFOD (Probability of failure on demand)

> The likelihood that the system will fail when a service request is made. A POFOD of 0.001 means that 1 out of a thousand service requests may result in failure

- **probability** that the **system will fail** when a service request is made
- Appropriate for protection systems where services are demanded occasionally and where there are serious 
consequences if the service is not delivered

### ROCOF (Rate of failure occurrence)

>The frequency of occurrence with which unexpected behaviour is likely to occur. A ROCOF of 2/100 means that 2 failures are likely to occur in each 100 operational time units. This metric is sometimes called the failure intensity

- **Rate** of **occurrence of failure** in the system
- Relevant for operating systems, transaction processing systems where the **system has to process a large number of similar requests that are relatively frequent**

---

## Availability definition

`The ability of an item to be in a state to perform a required function at a given instant of time or at any instant of time within a given time interval, assuming that the external resources, if required, are provided.`

- Measure of the **fraction of the time** that the **system is available for use**
- Takes repair and restart time into account
- **Relevant for** non-stop, continuously running systems

### MTTF (Mean Time To Failure)

> The average time between observed system failures.

> An MTTF of 500 means that 1 failure can be expected every 500 time units

- Measure of the **time between observed failures of the system**. Is the **reciprocal of ROCOF** for stable systems
- **Relevant for systems with long transactions** i.e. where system processing takes a long time. MTTF should be  longer than transaction length

### AVAIL

> The probability that the system is available for use at a given time. 

> Availability of 0.998 means that in every 1000 time units, the system is likely to be available for 998 of these

## Safety assurance
>  show that the system cannot reach an unsafe state

- Based on proof by contradiction

## Security assessment
- demonstrate that the system cannot enter some state (an unsafe or an insecure state)
- Security problems are more generic, many systems suffer from the same problems


## Safety vs Security
-  **Safety** defends the environment from *damages due to computer systems*
-  **Security** defends computer systems from *damages due to malicious users*



[Return Index](./README.md)