**Reliability:**
Continuing to work correctly, even when things go wrong. Things going wrong are called faults.

- Fault: when a component deviating from its specification
- Failure: when a system stops providing the required service to the user.

***Types of Fault***
Hardware Faults: Hard disks crash, RAM becoming faulty, power grid blackout. Hardware redundancy is usually used to reduce such faults (but not eliminate them completely). Fault tolerant techniques are used in addition to redundancy to further raise the tolerancy of such failures when they do happen.

Software/Systematic Faults: Software bugs, runaway process that uses up shared resources, cascading failures. Unlike hardware faults that affect only a single machine/hardware, systematic faults affect are not random or independent as they affect all machines in the cluster. Extensive testing and careful thinking through edge cases help to reduce the occurrence of such faults. 

Human Error: Humans are generally unreliable, thus processes that are done by humans are prone to errors. For example, configuration errors, etc. There are several approaches that can help- design systems in ways that minimize errors, test thoroughly at all levels, etc..

**Scalability:**
In simple terms, it means coping with increased load. Answering questions like if the system grows by X, what are the options for coping with the growth. How can we add computing resources to handle additional load? In discussing scalability, we need to describe load and performance.
- What is load? System load can be described using load parameters that depend on the architecture of the system. Example load parameters include: requests/sec to a web server, ratio of reads to writes in a db, hit rate on a cache, etc..
- What is system performance