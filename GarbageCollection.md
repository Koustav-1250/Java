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

Understanding the various aspects of garbage collection is essential for optimizing memory usage and developing efficient Java applications.
