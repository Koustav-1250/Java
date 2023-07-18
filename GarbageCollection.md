## Garbage Collection in Java

Garbage Collection (GC) is a crucial process in Java that removes objects stored in the heap memory when they no longer have any references. The Java Virtual Machine (JVM) decides when to perform garbage collection based on various factors.

- **Calling the Garbage Collector**: We can explicitly call the garbage collector in our program using the `System.gc()` method. However, it's important to note that the JVM has its own logic to determine the optimal time for garbage collection, and manual invocation should be used judiciously.

- **Marking and Sweeping**: JVM utilizes two main strategies to identify unreferenced objects:

  1. **Marking**: This process involves identifying objects that are directly or indirectly referenced by the stack memory. It marks all live objects and treats the remaining unreferenced objects as "islands of isolation." Previously, a counting method was used, but it faced challenges with cyclic dependency of object references.

  2. **Sweeping**: This technique is employed by the JVM to remove the unreferenced objects. There are three different approaches:

     - **Normal Sweeping**: This method takes extra memory but requires fewer steps than other approaches.
     - **Sweeping with Compacting**: It consumes more memory but involves an additional step of compacting the memory to optimize space.
     - (Incomplete point)
    
- STOP THE WORLD: While marking the objects for garbage collection, the java application is paused. (Think Why ;) )
  - There is alternative to this which is known as Concurrent garbage collector that run along side the application.
- JVM has five implementations of Garbage Collector
  - serial GC:
      a) Young generation: mark and copy strategy
      b) old generation: mark compact and sweep
      c) stop the world
      d) runs on single thread
  - paralled GC:
      a) Young generation: mark and copy strategy
      b) old generation: mark compact and sweep
      c) stop the world for less time than for serial GC
      d) running on mutiple thread
  - Concurrent Mark Sweep (CMS) GC
  - Garbage First GC (G1GC)
      a) Keeps tract of amount of live and dead objects
      b) divides heap in smaller regions
      c) not only concurrent but also parallel support
      d) aims for short pauses possible
      e) running on multiple threads
      f) concurrent and stop the world
      g) best for high performace applications and large memory space
  - Z GC
      a) max of 10 ms pauses
      b) uses reference coloring
  - **Metrics in GC**
       - Allocation rate: how fast the application allocates objects in memory.
       - Heap population
       - Mutation rate: How often the refrences are updated in the memory
       - Object life span
       - Mark time and Compaction time -> how long GC takes to mark the objects and free up the space and reallocates the space in memory
      

Understanding the various aspects of garbage collection is essential for optimizing memory usage and developing efficient Java applications.
