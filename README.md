# Operating Systems

* [ ] 

---

## Repo Summary

This repository contains hands-on work from the Operating Systems course: CPU scheduling simulators, shell scripts for basic system tasks, and programs that read Linux kernel and system state.

### Lab 1 — CPU scheduling

Simulation of classic **process scheduling algorithms** with arrival time, burst time, and (where applicable) priority and time quantum:

- **FCFS** (First-Come First-Served)
- **SJF** (Shortest Job First)
- **SRTF** (Shortest Remaining Time First)
- **Priority scheduling**
- **Round Robin**

Two variants are included:

- `os.cpp` — interactive menu-driven version (algorithm choice, number of processes, arrival/burst times).
- `copy_os.cpp` — streamlined version with the same algorithms, designed for scripted or automated runs (e.g. fixed input format).

Output includes waiting time, response time, turnaround time, and throughput per process.

See **[Lab 1/README.md](Lab%201/README.md)** for build and run instructions.

---

### Lab 3 — Shell scripting

A set of **Bash scripts** used for OS lab exercises:

| Script          | Description                                                         |
| --------------- | ------------------------------------------------------------------- |
| `swap.sh`     | Swap two numbers without a temporary variable.                      |
| `prime.sh`    | Check if a number is prime.                                         |
| `odd_even.sh` | Check if a number is odd or even.                                   |
| `leap.sh`     | Leap year check (divisible by 4, 100, 400 rules).                   |
| `area.sh`     | Circle area and circumference (radius input).                       |
| `files.sh`    | Create and remove 20 dummy files (`file1.txt` … `file20.txt`). |
| `content.sh`  | Compare two files (`W1.txt`, `W2.txt`) with `cmp`.            |
| `cprog.sh`    | Find all `.c` files in a folder, compile and run each one.        |

The **`test/`** subfolder contains a sample C file used with `cprog.sh`. Some scripts (e.g. `content.sh`) expect files like `W1.txt` and `W2.txt` in the same directory — see **[Lab 3/README.md](Lab%203/README.md)** for details.

---

### Lab 4 — Linux `/proc` and system monitoring

Two C++ programs that use the Linux **`/proc`** filesystem and standard CLI tools:

1. **`proc_parser1.cpp`**Prints basic system info:

   - CPU model name (`/proc/cpuinfo`)
   - Kernel version (`uname -r`)
   - Total memory (`/proc/meminfo`)
   - Uptime (`uptime -p`)
2. **`proc_parser2.cpp`**Simple **system monitor**: samples at a configurable interval and reports averages for:

   - CPU time in user mode, system mode, and idle
   - Context switch rate
   - Free memory
   - Process creation rate

   Uses `vmstat`, `top`, `ps`, and `/proc/meminfo`; input is print rate and read rate (see **[Lab 4/README.md](Lab%204/README.md)**).

**Note:** These programs are written for **Linux** (they rely on `/proc` and tools like `vmstat`/`top`). They will not run as-is on macOS or Windows.

---

## Guest lecture — CS3102 Operating Systems

The year after taking this course, I was invited to give a **guest lecture** for the same course (CS3102 Operating Systems). The talk focused on:

- **Real world applications of OS concepts** — how ideas from the course show up in practice.
- **Algorithms behind concurrent collaborative systems** — coordination, synchronization, and consistency in multi user and distributed settings.
- **Real time scheduling techniques** — timing guarantees, priorities and trade offs in real time and embedded systems.

It was a chance to connect the theory and labs (scheduling, processes, concurrency) to systems students might build or encounter in industry and research.

---

## Shoutout & Recommended Reading

**Ananta Srikar** introduced me to the book **[*Operating Systems: Three Easy Pieces*](https://ostep.org)** (OSTEP). It was a major help for building intuition and for connecting concepts to the labs.

If you’re interested in OS, whether you’re taking a course or exploring on your own I strongly recommend reading **Operating Systems: Three Easy Pieces**. It’s available [free online](https://ostep.org) and is one of the clearest and most practical introductions to the topic.

---

## Repository structure

```
Operating_Systems/
├── Lab 1/          # CPU scheduling (C++)
│   ├── os.cpp
│   ├── copy_os.cpp
│   └── README.md
├── Lab 3/          # Shell scripts (Bash)
│   ├── *.sh
│   ├── test/
│   └── README.md
├── Lab 4/          # /proc parsers & system monitoring (C++, Linux)
│   ├── proc_parser1.cpp
│   ├── proc_parser2.cpp
│   └── README.md
├── LICENSE
└── README.md
```

Each lab folder has its own **README** with usage and, where relevant, build/run instructions.

---

## License

This project is licensed under the **Apache License 2.0** — see [LICENSE](LICENSE) for details.
