CS3502 Project 1 - Multi-Threaded Programming

Overview
This project demonstrates several important concepts in concurrent programming using POSIX threads in C. The project consists of four phases that illustrate race conditions, mutex synchronization, deadlock creation, and deadlock prevention.

Phase Descriptions

Phase 1: Race Condition
Two threads modify a shared variable without synchronization. Because the threads access the variable concurrently, the final result can vary between program executions.

Phase 2: Mutex Synchronization
A mutex lock is added to protect the shared variable. This ensures that only one thread modifies the variable at a time, eliminating the race condition.

Phase 3: Deadlock Demonstration
Two threads acquire two mutex locks in opposite order. This creates a circular wait condition and causes the program to deadlock.

Phase 4: Deadlock Prevention
Both threads acquire the mutex locks in the same order, preventing circular waiting and eliminating the deadlock.

Compilation

gcc -Wall -Wextra -pthread phase1.c -o phase1
gcc -Wall -Wextra -pthread phase2.c -o phase2
gcc -Wall -Wextra -pthread phase3.c -o phase3
gcc -Wall -Wextra -pthread phase4.c -o phase4

Execution

./phase1
./phase2
./phase3
./phase4

Author
Shamal Khattak

Repository
https://github.com/MrCoder1218/cs3502-project1
