# Performance

## TOC

* this doc overviews the performance
  * tool: [instruments](instruments) overview

## Categories of Performance Problems

Aspect | Problems | Answers (Programming) | Tools - Instruments | WWDC
--|--|--|--|--
Memory | (Leaks and over-released led crash) | ARC, avoid retain cycle. | ASan | 2015-413
CPU/Speed , on UI/Graphics | Slow and irresponsive | multi-threading, | Time Profiler |
Energy | inefficient | ... | 2014-710 2014-712 2016-720
Local Access (Filesystem, CoreData) | Slow | Usage control |
Network Access |
Threading / Concurrency | metex, data race, incorrect data | GCD | TSan | 2016-720


## Quick tips

* prioritize work with GCD/Dispatch
