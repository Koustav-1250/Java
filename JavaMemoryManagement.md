- Java uses two major memory -> stack memory and heap memory.
- Stack memory stores the primative data types and reference variables to objects.
- Objects are stored in heap memory.
- Heap memory has three generations
    a) Young generation: It has newly created objects
    b) Survivor generation: It has objects that are still has reference for some time. The unreferences one from young generation will get deleted by garbage collector and the remaining
       will move to survivor generation.
    c) Old generation: The objects that is referenced for longer duration of time comes to this space.
    Metaspace: Here we store the metadata of the object for ex. class structure, annotations etc.
