
## Types of Instruments

* __Activity Monitor__, monitors processes' CPU, memory, disk, and network usage statistics.
* __Allocations__, tracks a process' anonymous virtual memory and heap, providing class names and optionally retain/release histories for objects.
* __Cocoa Layout__, observes changes to NSLayoutConstaint objects to help determine when and where a layout constraint went awry.
* __Core Animation__, measures application graphics performance as well as CPU usage of a process via time profiling.
* __Core Data__, traces Core Data filesystem activity, including fetches, cache misses, and saves.
* __Counters__, collects performance monitor counter (PMC) events using time or event based sampling methods.
* __Energy Log__, provides diagnostics regarding energy usage as well as basic on/off state of major device components.
* __File Activity__, monitors file and directory activity, including file open/close calls, file permission modifications, directory creation, file moves, etc.
* __Leaks__, measures general memory usage, checks for leaked memory, and provides statistics on object allocations by class as well as memory address histories for all active allocations and leaked blocks.
* __Metal System Trace__, profiles the performance of iOS, tvOS, and macOS Metal applications by providing tracing information from the application, driver, and GPU layers.
* __Network__, analyze how your applications are using TCP/IP connections using the Connections instrument.
* __System Trace__. A comprehensive view of what's happening in the operating system. See how threads are being scheduled across CPUs and understand how system calls and virtual memory faults are affecting your application's performance.
* __System Usage__, records I/O system activity related to files, sockets, and shared memory for a single process launched via instruments. Inputs, outputs, duration, backtrace, calltree, etc. is provided for each call.
* __Time Profiler__, performs low-overhead time-based sampling of processes running on the system's CPUs.
* __Zombies__, measures general memory usage while focusing on the detection of over-released "zombie" objects. Also provides statistics on object allocations by class as well as memory address histories for all active allocations.


## Guides

* [Instruments User Guide](https://developer.apple.com/library/content/documentation/DeveloperTools/Conceptual/InstrumentsUserGuide/index.html#//apple_ref/doc/uid/TP40004652-CH3-SW1)
