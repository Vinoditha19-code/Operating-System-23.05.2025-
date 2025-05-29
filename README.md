# Operating-System-23.05.2025-

01. Read three integers (a, b, c) from the user.
Use two child processes to compute:
  The factorial of a.
  The Fibonacci series up to b terms.
  The prime check for c.

* This program demonstrates how to utilize multiple processes to perform different computational tasks in parallel.
* Using fork(), you create two child processes, allowing tasks to run concurrently, which reflects a basic form of parallel processing.
* Each child process handles a distinct job, showcasing how to split workload across processes.

02.  This program demonstrates the use of multiple processes (via fork()) to perform parallel computations on a single input number n. It performs the following computations using child processes:
Factorial of n
Fibonacci term at position n
2 to the power of n
Square of n

The main process (parent) takes user input (n).
It creates Child1, which calculates the factorial of n.
    Inside Child1, another process (Child5) is forked to calculate the Fibonacci term at position n.
Meanwhile, the parent also forks:
    Child2, which computes 2ⁿ.
    Child3, which computes the square of n.
Each child process:
    Prints its PID and PPID.
    Executes its assigned arithmetic task.
    Then terminates.
The parent process waits (wait(NULL)) for all child processes to complete, ensuring synchronization.
