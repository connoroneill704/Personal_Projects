# Operating System Kernel and Device Services

A multi-phase operating systems project implemented in C using the USLOSS
simulated operating-system environment.

The project builds core kernel functionality including process management,
priority scheduling, interprocess communication, system calls, clock services,
terminal I/O, and disk I/O.

## Technologies and Concepts

- C
- Linux
- USLOSS operating-system simulator
- Kernel and user modes
- Process scheduling and context switching
- Interprocess communication
- Mailboxes and synchronization
- Interrupt handling
- System calls
- Terminal and disk device I/O

## Features

### Process Management

- Created and maintained process control blocks
- Implemented process creation, termination, joining, and parent-child tracking
- Managed process states and priority-based ready queues
- Performed context switching between processes
- Supported process blocking and unblocking

### Interprocess Communication

- Implemented mailbox-based communication
- Supported blocking and conditional send and receive operations
- Used mailboxes for synchronization and mutual exclusion
- Coordinated communication between kernel services and daemon processes

### User-Mode System Calls

- Implemented syscall handlers connecting user-mode programs to kernel services
- Supported process creation, termination, waiting, and process information
- Validated arguments and handled user/kernel mode transitions

### Clock and Sleep Services

- Implemented a wake-time-ordered sleeping-process queue
- Used clock interrupts and a daemon process to track elapsed time
- Blocked and awakened processes according to requested sleep durations

### Terminal Services

- Implemented terminal read and write system calls
- Buffered terminal input by line
- Used interrupts and mailboxes to coordinate terminal input and output
- Supported multiple terminal units with synchronization

### Disk Services

- Implemented disk read, write, seek, and disk-size operations
- Supported multi-sector operations across track boundaries
- Used disk daemons and interrupt-driven device communication
- Protected disk access with mailbox-based locks

## Project Files

- `phase1.c` — process management, scheduling, and context switching
- `phase1b.c` — extended process control and blocking services
- `phase2.c` — mailbox-based interprocess communication
- `phase3.c` — user-mode process and system-call services
- `phase4a.c` — clock, terminal, and initial disk services
- `phase4b.c` — completed clock, terminal, and disk implementation
- `phase1.h`, `phase4.h` — project interfaces and declarations

## Collaboration

This project was completed collaboratively by Connor O'Neill and Waldo Guzman
as part of an operating systems course at the University of Arizona.

## My Contributions

- Contributed to implementing and debugging process-management and scheduling logic
- Helped develop mailbox-based synchronization and interprocess communication
- Implemented and tested clock, terminal, and disk system-call services
- Debugged interrupts, blocking behavior, device operations, validation, and integration issues

## Build Requirements

The source files depend on the USLOSS course framework, including provided
headers, libraries, test cases, and build infrastructure that are not included
in this portfolio repository.

The files are included to demonstrate the student-written kernel and device
service implementations and are not intended to compile independently.