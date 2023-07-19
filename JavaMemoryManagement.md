## Java Memory Management

Java employs two major types of memory: stack memory and heap memory.

- **Stack Memory**: This memory segment stores primitive data types and reference variables to objects. It is organized in a stack-like structure, where variables are pushed and popped as method calls are made and returned.

- **Heap Memory**: Objects in Java are stored in the heap memory. It is a dynamically allocated memory segment that provides more flexibility than stack memory. The heap memory is managed by the garbage collector, which automatically reclaims memory for objects that are no longer referenced.

Heap memory is further divided into three generations:

1. **Young Generation**: 
    a) Eden Space: This space holds newly created objects. It is further divided into an Eden space and two survivor spaces. Objects initially reside in the Eden space, and some of them are moved to survivor spaces during garbage collection.

    b). Survivor space*: Survivor spaces hold objects that have survived one or more garbage collection cycles. Objects that are still referenced will be moved between survivor spaces in subsequent garbage collection cycles.

2. **Old Generation**: The old generation, also known as the tenured generation, contains objects that are referenced for a longer duration of time. These objects have survived multiple garbage collection cycles and are more stable.

Additionally, Java has a **Metaspace** (previously known as Permanent Generation) where metadata related to classes, methods, and annotations is stored. It dynamically expands to accommodate class metadata, reducing the risk of memory-related errors.

Understanding Java's memory management is crucial for efficient application development and optimizing resource utilization.
