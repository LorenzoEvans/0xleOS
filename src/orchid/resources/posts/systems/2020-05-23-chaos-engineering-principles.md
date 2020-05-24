---
title: 'Principles of Chaos Engineering notes'
tags:
    - systems
    - programming
    - chaos-engineering
notes: true
---

<i>from:</i> [Principles of Chaos Engineering](https://principlesofchaos.org/?lang=ENcontent "Principles of Chaos Engineering")
# Abstract:
- <i>Advances in large scale, distributed systems are changing the nature of software engineering.</i>
- <i>How much confidence can we have in the complex systems that we put into production?</i>
- <i><b>Even when all of the individual components of a (distributed) system are working correctly, the interactions can be unpredictable.</b></i>
This is <i>sometimes</i> (referred to as) emergent behavior.
- <i>Unpredictable behavior, and real-world events that can affect production environments, and can make distributed systems chaotic.</i>
- <i>Weaknesses should be identified before they manifest unexpected behavior throughout the system.</i>
# System Weaknesses could be:
- </i>Improper fallback (failover) settings when a service becomes unavailable.</i>
- </i>Retry storms from improperly tuned timeouts.</i>
- </i>Outages when downstream dependencies receive too much traffic.</i>
- </i>Cascade failures when a Single-Point-Of-Failure goes down.</i>

<b>An empirical systems-based approach to managing the *chaos* in distributed systems will build confidence in their ability to withstand realistic conditions.</b>

# Chaos In Practice:
- __To specifically address the uncertainty, we use experiments that follow four steps:__
    - Start by defining #steady-state as some measurable output of a system that indicates it is healthy.
    - Hypothesize that this steady state will continue in both the control and experiment group.
    - Introduce variables that reflect real world effects, such as crashes, hard drive failures, severed network connections.
    - Try and disprove the hypothesis by looking for a difference in the  steady-state group, and the experimental group.
- __The harder it is to disrupt the steady-state, the more confident we can be in the behavior of the system.__
- __If a weakness is exposed, you have a target for improving, and thus increasing the resiliency of your system.__

- # Advanced Principles:
    -  __The following principles describe an ideal application of Chaos Engineering, and the degree to which they are applied strongly correlates to the confidence we can have in a distributed system.__
    -  **Build a Hypothesis around Steady State Behavior.**
        - Focus on the measurable output of a system, rather than the internal attributes- measurements of a systems output over time constitute a proxy for the system's steady-state.
        - The system's throughput (IOPS), error rates, latency-percentiles, could all be metrics of interest for representing steady-state behavior.
        -  __By focusing on system behavior patterns, chaos-engineering verifies that a system__ **__does__** work, rather than validating **how** it works.
    -  **Vary Real-World Events.**
        - Chaos variables should reflect real-world events.
        - Prioritize events by potential impact, or frequency.
        - Consider events that correspond to to hardware failures.
        - Any event capable of disrupting a steady state system is a potential chaos variable.
    -  **Run Experiments in Production.**
        - Systems behave differently depending on environment and traffic.
        - The only traffic that can properly mimic the randomness of real traffic is real traffic.
        - To guarantee authenticity in both the experiment and relevance to the current system, prefer testing on production traffic.
    -  **Automate Experiments to Run Continuously**
        - Running experiments manually is labor intensive, and doesn't scale.
        - #CE builds automated experimentation into the system to drive both orchestration and analysis.
    -  **Minimize Blast Radius**
        - Experimenting on production can affect user experience. 
        - While there must be some allowance for short term negative impact, ensure that the fallout from experiments are properly contained and mitigated.
