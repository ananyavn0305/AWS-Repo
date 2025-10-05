## Easy Level

1. **What are EC2 instance types?**  
   EC2 instance types define combinations of CPU, memory, storage, and networking capacity.

2. **Why are there different EC2 instance types?**  
   To suit different workloads such as compute-intensive, memory-intensive, or storage-heavy applications.

3. **Name some popular EC2 instance families.**  
   General Purpose, Compute Optimized, Memory Optimized, Storage Optimized, and Accelerated Computing.

4. **What is the general-purpose instance family used for?**  
   Balanced compute, memory, and networking—ideal for web servers and small databases.

5. **What does the 't' in t2.micro stand for?**  
   It belongs to the “General Purpose” instance family.

6. **What is a burstable performance instance?**  
   Instances that provide baseline CPU performance with the ability to burst above it temporarily.

7. **Give an example of a compute-optimized instance.**  
   c5.large, c6g.xlarge, etc.

8. **What is the main benefit of compute-optimized instances?**  
   High performance for compute-bound applications.

9. **Give an example of a memory-optimized instance.**  
   r5.large, x1e.xlarge, etc.

10. **What workloads are memory-optimized instances best for?**  
    In-memory databases, real-time big data analytics.

## Moderate Level

11. **Give an example of a storage-optimized instance.**  
    i3.large, d2.xlarge, etc.

12. **What is the use case for storage-optimized instances?**  
    High, sequential read/write access to large data sets.

13. **What is an accelerated computing instance?**  
    Instances using hardware accelerators like GPUs or FPGAs for compute-heavy tasks.

14. **Give an example of an accelerated computing instance.**  
    p3.2xlarge, g4dn.xlarge, etc.

15. **What type of workloads use GPU instances?**  
    Machine learning, graphics rendering, and deep learning.

16. **What is the main advantage of ARM-based Graviton instances?**  
    Better performance per watt and cost efficiency.

17. **What does the 'm' in m5.large represent?**  
    It belongs to the General Purpose “m” family.

18. **What does the 'r' in r5.large stand for?**  
    “R” stands for memory-optimized.

19. **What does the 'c' in c5.large stand for?**  
    “C” stands for compute-optimized.

20. **What is the 'i' instance family used for?**  
    “I” stands for I/O optimized, used for high storage performance.

21. **What does the ‘g’ in g4dn stand for?**  
    GPU (graphics) accelerated instance family.

22. **What does the 'x' instance family indicate?**  
    Extra large memory instances for enterprise databases or SAP workloads.

23. **What are T-series instances used for?**  
    Low-cost, burstable workloads like small web apps and development environments.

24. **What are M-series instances used for?**  
    Balanced workloads such as medium-size databases and caching servers.

25. **What are C-series instances used for?**  
    High compute performance workloads like video encoding and gaming servers.

26. **What are R-series instances used for?**  
    High memory workloads such as caching and real-time big data processing.

27. **What are I-series instances used for?**  
    High-performance, low-latency storage workloads.

28. **What are G-series instances used for?**  
    Machine learning inference and graphics rendering.

29. **What are P-series instances used for?**  
    Deep learning training and high-performance GPU computing.

30. **What is the naming convention of EC2 instances?**  
    `<Family><Generation>.<Size>` — e.g., m5.large.

31. **What does the size suffix (small, large, xlarge) represent?**  
    The relative capacity of CPU and memory.

32. **What is the main difference between m5 and m6g instances?**  
    m6g uses ARM-based Graviton processors, while m5 uses Intel Xeon.

33. **What is the difference between i3 and i3en instances?**  
    i3en provides higher network and storage performance than i3.

34. **What is the 'd' instance family used for?**  
    Dense storage workloads.

35. **What are HPC instances?**  
    High-performance computing instances designed for scientific simulations or modeling.

36. **Which instance type would you use for batch processing?**  
    Compute-optimized (C-series).

37. **Which instance type is ideal for analytics workloads?**  
    Memory-optimized (R-series or X-series).

38. **Which instance type is ideal for rendering 3D graphics?**  
    GPU-based (G-series or P-series).

39. **Which instance type is recommended for SAP HANA?**  
    X1e or X2 instances.

40. **Which instance type supports Elastic Fabric Adapter (EFA)?**  
    Some C5n, M5n, R5n, and HPC instance families.

## Hard Level

41. **What is the difference between shared and dedicated instance tenancy?**  
    Shared instances share hardware with others; dedicated instances use isolated hardware.

42. **What is a bare-metal instance in EC2?**  
    It gives direct access to underlying physical hardware without virtualization.

43. **Which instance family supports bare-metal configurations?**  
    M5, C5, R5, i3, and others have bare-metal variants.

44. **What is Enhanced Networking in EC2?**  
    A feature that provides higher bandwidth and lower latency using SR-IOV.

45. **Which instance types support Enhanced Networking?**  
    Most modern instance families like C5, M5, R5, and T3.

46. **What are the network performance tiers in EC2?**  
    Low, Moderate, High, and 10–100 Gbps dedicated bandwidth options.

47. **What does vCPU mean in EC2?**  
    Virtual CPU — one thread of a physical core available to the instance.

48. **How can you choose the right EC2 instance type?**  
    Based on workload requirements — CPU, memory, storage, and network performance.

49. **Can you change the instance type after launching?**  
    Yes, stop the instance, modify the type, and restart it.

50. **Which EC2 instance type is best for web servers?**  
    General purpose instances like t3.micro or m5.large.
