-  GC
  - It is used to remove the objects stored in heap memory which has no reference.
  - JVM decides when we want to process garbage collection.
  - System.gc() is one way we can call garbage collector in our program
  - So there are two strategies in which jvm finds out not used objects i.e MARKING and SWEEPING
      * So firstly we find out which object is having reference to stack memory and then we find the nested reference to that object in heap memory. Basically marking
        all the objects that are live directly and indirectly. The remaining unreferenced objects are defined as island of isolation.
      * Older way garbage collection was done using counter method. But the cyclic dependecy of object reference was the problem in this method.
      * Sweeping is technique that JVM does to remove the unreference objects. So there are 3 ways it does,
        a) normal sweeping -> takes extra memory but takes less steps than b.
        b) sweeping with compacting -> more memory but takes one extra step of make the memory compact.
        c) 
