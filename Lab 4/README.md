# Lab 4 — /proc parsers & system monitoring

C++ programs that use the Linux **`/proc`** filesystem and standard tools. **Linux only** (not macOS/Windows).

## Files

- **`proc_parser1.cpp`** — Prints: CPU model name, kernel version, total memory, uptime. No input; just run.
- **`proc_parser2.cpp`** — Samples system metrics at a given interval and prints averages: user/system/idle CPU %, context switch rate, free memory, process creation rate. Prompts for **print rate** (total time to run, in seconds) and **read rate** (seconds between samples).

## Build

```bash
g++ -o proc_parser1 proc_parser1.cpp
g++ -o proc_parser2 proc_parser2.cpp
```

## Run

```bash
./proc_parser1
./proc_parser2   # then enter e.g. print rate 10, read rate 2
```

## Dependencies

- Linux with `/proc`
- Commands used: `grep`, `uname`, `uptime`, `vmstat`, `top`, `ps`, `awk`. These are standard on most Linux installations.
