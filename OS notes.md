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

# Resource Allocation
- Resource is hardware or software that is needed to complete a task.
- Allocation is to assign resources to certain programs in the computer. maloc
- De-allocation is to release resources when the task is complete. freemem

# Allocating the CPU
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
      - Program A and B are running, program A needs to read something, so program A generates an interrupt, normal processing is temporarily suspended and the CPU focuses on the the read operation, while waiting for the read to complete, the CPU begins processing program B. When the read operation is complete, another interrupt is generated, then normal processing is temporarily suspended and the CPU looks at the interrupt and determines its cause. Then the CPU which program to focus priority on.
  - Time-sharing Multiprogramming
    - One program receives the attention of the CPU
    - A small fraction of CPU time is allocated to the program
    - the time slice ends, then begins processing another program
    
- More than 1 CPU
  - Multiprocessing / multiple CPU running several programs simultaneously.
  
# Sharing Memory
- Program must be in memory to be executed
- Problems
  - Programs compete for space
  - may have a large program 
  - The memory space for each program must not overlap
  
# Memory Management
- Providing separate memory of space to programs
- Memory protections keeps one programs from interfering with another
  - Partitions or regions
    - Divide memory into sections
    - The partition must accommodate the largest possible program
    - Might cause wasted memory space
  - Foreground and background
    - Programs are placed in either foreground or background
    - Programs in Foreground have priorty for CPU time
    - While performing read/write operations for the Foreground program, the CPU gives time to a program in the Background
    - Programs are palced in a holding queue while waiting to run.
  - Virtual storage(virtual memory)
    - Uses paging
      - Divide the program into equal-size pieces (pages)
      - Store each piece in equal-size memory spaces (pages frame)
      - Typical size is 2KB or 4KB
      - Create an index to each page and store in a page table
      - A portion of the program is placed in memory
      - The remainder is on disk
      - Sections on disk will be brought into memory as needed one page at a time.
    - Problem / Thrashing
      - too large a portion of CPU time is spent locating the correct page and brining into memory.
      - solution is to run fever programs concurrently or add memory.
# Memory Protection
- Keeps one program from straying into another
- Confines each program to certain defined limits in memory
- Neccessary because it is possible for a program to be saved onto another program if its transferred to the wrong memory location, possible wiping or destroying of data.
- Terminate program is assigned memory space is already used.

# Sharing Storage
- Several users need to access the same disk pack/ one wants to write, the other read.
- OS keeps track of the I/O requests and processes them in the order received.

# Sharing Printing Resouces
- Print resources are shared between active programs
- Printouts are generated in pieces as the CPU gives each concurrent program some time.
- Problem is that the current program may generate a few print lines and the cpu moves to the next program and the 2nd program may generated a few print lines.
- The printers are also slow compared to the CPU speed.
- Solution is that the CPU writes to the disk and the program will complete faster.

# Utility Programs
- Come with System Software
- Handles special needs
- Perform secondary chores
- Do not need to be memory resident
- Disk defragmenter reorganizes files so they are stored contiguously on disk providing for faster access
- Device drivers convert operating system instructions into commands that are know to a specific device
