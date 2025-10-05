## Easy Level

1. **What is virtualization?**  
   Virtualization is the process of creating multiple virtual machines on a single physical machine to maximize resource utilization.

2. **What is a hypervisor?**  
   A hypervisor is a software layer that manages virtual machines and allocates resources from the host system.

3. **What is a virtual machine (VM)?**  
   A virtual machine is an isolated software-based computer that runs its own OS and applications on virtualized hardware.

4. **What is the host machine?**  
   The host machine is the physical computer on which virtual machines are created and executed.

5. **What is the guest machine?**  
   The guest machine is the virtual instance running on a host machine via a hypervisor.

6. **What is the function of a hypervisor in virtualization?**  
   It divides and allocates the physical system’s resources among multiple virtual machines.

7. **Name the two types of hypervisors.**  
   Type 1 (Bare-metal) and Type 2 (Hosted).

8. **What is a data center?**  
   A data center is a physical facility that stores and manages computing and networking equipment.

9. **What is an AWS Region?**  
   A Region is a geographical area containing multiple AWS data centers called Availability Zones.

10. **What is an Availability Zone (AZ)?**  
    It’s an isolated data center within an AWS Region designed for high availability and fault tolerance.

## Moderate Level

11. **Differentiate between Type 1 and Type 2 hypervisors.**  
    Type 1 runs directly on hardware; Type 2 runs on an operating system.

12. **Why is virtualization important in cloud computing?**  
    It allows efficient resource utilization and enables multiple OSes on a single machine.

13. **How does virtualization improve scalability?**  
    It allows quick creation and deployment of virtual machines as demand increases.

14. **Explain how a hypervisor isolates VMs.**  
    It assigns separate memory and CPU slices to each VM, ensuring no interference.

15. **What are the main components of a data center?**  
    Compute, storage, and networking equipment.

16. **Why does AWS use multiple Availability Zones per Region?**  
    To ensure fault tolerance and redundancy.

17. **How does virtualization enhance hardware utilization?**  
    By enabling multiple workloads to share the same hardware resources.

18. **What role does a hypervisor play in managing virtual machines?**  
    It creates, runs, monitors, and deletes VMs as needed.

19. **What is the purpose of regions in AWS?**  
    They allow users to deploy applications closer to customers for lower latency.

20. **How does AWS ensure reliability using Availability Zones?**  
    Each zone operates independently with separate power and networking systems.

## Hard Level

21. **Explain the full virtualization process.**  
    Full virtualization uses a hypervisor to emulate complete hardware, allowing unmodified OSs to run.

22. **What challenges does virtualization introduce in resource allocation?**  
    It may cause performance overhead due to shared resource contention.

23. **What is paravirtualization?**  
    A method where the guest OS communicates directly with the hypervisor for better performance.

24. **Explain nested virtualization.**  
    Running a virtual machine inside another virtual machine.

25. **How does AWS handle data center redundancy?**  
    Through multiple AZs across regions for backup and fault recovery.

26. **Describe the AWS global infrastructure hierarchy.**  
    Global → Region → Availability Zone → Data Center → Server.

27. **What are the performance impacts of using Type 2 hypervisors?**  
    They’re slower because they depend on the host OS for hardware access.

28. **How does AWS achieve high availability across multiple regions?**  
    By replicating data and workloads across multiple geographically separated AZs.

29. **Explain the difference between compute and storage in a data center.**  
    Compute handles processing tasks; storage manages data persistence.

30. **What are the key security considerations in virtualization?**  
    Isolating VMs properly, securing hypervisors, and managing access control.
