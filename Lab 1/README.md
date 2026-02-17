# Lab 1 — CPU scheduling

Simulates classic process scheduling algorithms with configurable processes (arrival time, burst time, priority, time quantum).

## Files

- **`os.cpp`** — Interactive: prompts for scheduling algorithm (1–5), number of processes, arrival times, burst times, and (for Priority) priorities. Implements FCFS, SJF, Priority; SRTF and Round Robin are stubbed.
- **`copy_os.cpp`** — Full implementation of all five algorithms. Expects input from stdin in a fixed format (see below).

## Build

```bash
# os.cpp
g++ -o os os.cpp

# copy_os.cpp
g++ -o copy_os copy_os.cpp -std=c++11
```

## Running

**os.cpp:** Run and follow the prompts (algorithm number, number of processes, arrival times, burst times, and priorities if you choose Priority).

**copy_os.cpp:** Input format:

1. Algorithm: `1` = FCFS, `2` = SJF, `3` = SRTF, `4` = Priority, `5` = Round Robin  
2. Number of processes `n`  
3. `n` arrival times (one per line or space-separated)  
4. `n` burst times  
5. If Priority (4): `n` priorities  
6. If Round Robin (5): time quantum

Example (FCFS, 3 processes):

```
1
3
0 1 2
5 3 2
```

Output: one line each for waiting times, response times, turnaround times, then throughput.
