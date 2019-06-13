# Memory Leaks

A condition that occurs due to a failure in a program to release discarded memory, causing impaired performance or failure.


## Common Symptoms

## Reasons

## How to find?

## How to resolve?

1. For PM2 users, the **max_memory_restart** option is available to automatically restart node processes when they reach a certain amount of memory


## Tools to debug

1. heapdump - library to write snapshot of heap to file
- memwatch - helps in comprehensive memory analysis with leak, stat events. HeapDiff lets compare the heap usage at different points
