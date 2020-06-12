# Kernel

- Manages the Operating System
- Memory resident / always in main memory
- Loads programs that are between software and hardware
- Controls non-resident portions of the OS

# Booting
- Loads the kernel into memory.

# Systems Software
## Operating System
- Manages resources such as CPU, Disk drives, memory.
- Gives UI
- Execute software
- Does the input and output operations
- Different types such as command line, Single user PC, Network Operating System(NOS)
- NOS
  - Designed to permit computers on a network to share resources
  - Windows 2000 server
  - Novell Net Ware
  - Provides data security and administrative control
  - Functions
    - Split between client and server computers
    - Server / File management
    - Client, requests to the server, messageing, has its own local OS
    - Makes the resources appear as if they are local to the client's computer
- Large Computers
  - Used by many people at once
  - OS controls who gets to access resources and what keep the programs from diff users from getting mixed up

### User Interface
- Is the bridge between the user and the OS
- Command line / text-based, key commands MS-DOS
  - UNIX
    - Supports Multi-user 
    - Primarily used on Internet servers
    - Runs on various processors and many types of computers
  - Linux
    - Open source
    - More stable than windows, easy reinstallation
    - Scarce applications
- Graphical UI / Windows / on screen pictures

### Platform
- Computer hardware and operating system software that dictate what other softwares can run.
- Wintel 
  - Intel-based PC running Windows

### Resource Allocation
- Resource is hardware or software that is needed to complete a task.
- Allocation is to assign resources to certain programs in the computer. maloc
- De-allocation is to release resources when the task is complete. freemem

### Allocating the CPU
- One CPU
  - Multiprogramming, event driven and timesharing
    - Concurrent execution of two or more processes
    - Several processes open at once and only 1 process can be the priority of the CPU at a time
    - Effective because CPU speeds are many times fatter than input/output speeds
  - Event-driven Multiprogramming
    - One program receives the attention of the CPU
    - Its processing will be interrupted based upon events in the program
    - When processing needs to be temporarily suspended, an interrupt in generated
    - This is a signal to the operating system to evaluate the cause of the interrupt and determine who should now have CPU attention.
    - E.g.
      - program A and B are running, program A needs to read something, so program A generates an interrupt, normal processing is temporarily suspended and the CPU focuses on the the read operation, while waiting for the read to complete, the CPU begins processing program B. 
- > 1 CPU
  - Multiprocessing / multiple CPU running several programs simultaneously.
  

