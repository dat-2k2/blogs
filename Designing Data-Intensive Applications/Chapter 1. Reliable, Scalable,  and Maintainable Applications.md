---
layout: default
title: Chapter 1. Reliable, Scalable, and Maintainable Applications
parent: Designing Data-Intensive Applications
nav_order: 1
permarlink: /Chapter-1-Reliabled-Scalable-and-Maintainable-Applications
---

# Chapter 1. Reliable, Scalable, and Maintainable Applications
3 components of DIA:
- [Reliability](#reliability): The system should continue to work correctly (performing the correct
 function at the desired level of performance) even in the face of
 adversity (hardware or software faults, and even human error)
    - Tolerating hardware and software faults.
    - Human error.
- Scalability:  As the system grows (in data volume, traffic volume, or complexity),
 there should be reasonable ways of dealing with that growth.
    - Measuring load and performance.
    - Latency,percentiles, throughput.
- Maintainability: Over time, many different people will work on the system (engineering and operations, both maintaining current behavior and adapting the system to new use cases), and they should all be able to work on it *productively*.
    - Operability
    - Simplicity
    - Evolvability

Several main functionalities:
- Store data so that they, or another application, can find it again later (**databases**)
- Remember the result of an expensive operation, to speed up reads (**caches**)
- Allow users to search data by keyword or filter it in various ways (**search indexes**)
- Send a message to another process, to be handled asynchronously (**stream processing**)
- Periodically crunch a large amount of accumulated data (**batch processing**)

## Reliability
Also can be called **fault-tolerant/resilient**.

Fault is not same as failure. A *fault* is usually defined as one component of the system deviating from its spec, whereas a *failure* is when a system as a whole stops providing the required service to the user. 

It is impossible to make possibility of fault zero. Therefore, it is usually best to design fault-tolerance mechanisms that **prevent faults from causing failure**.

### Hardware Faults
- Mean time to failure (MTTF) of hard disk is 10 - 50y.

- Add redundancy to the individual hardware components in a system.
- However there's a move towar systems that can tolerate the loss of *entire machines*, e.g. several nodes in a cluster. 
    - This requires software technique in preference of in addition to hardware redundancy.

### Software errors



### Human errors
-  Design systems in a way that minimizes opportunities for error. 
-  Decouple the places where people make the most mistakes from the places where they can cause failures.
-  Test thoroughly at all levels, from unit tests to whole-system integration tests and manual tests.
- Allow quick and easy recovery from human errors, to minimize the impact in the case of a failure. 
- Set up detailed and clear monitoring, such as performance metrics and error rates.
- Implement good management practices and training. 



