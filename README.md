# BackingStore
The backing store is a virtual simulation of how memory is fetched in an operating system.  Yes, virtual simulation, because it's a simulation of how virtual memory is managed.  There are three flavors, the basic, one that implements a FIFO, and another that implements LRU.  "Memory" is written from a backing store, or a pretend file system.  The file is opened and read from when the program encounters a page fault, just like what would happen when an actual program encounters code that it doesn't have a pointer to.  In addition to a page table that holds a map from virtual page numbers to literal memory frames, there is also a TLB, or miniature, optimized page table for getting the most recently used frames.

This program is written entirely in C, a language which I have grown to love.  I made my own map structure for this assignment, which is implemented in the struct defined in main vm.c.  This assignment was also created during one of my favorite classes while I was in college, operating systems.
