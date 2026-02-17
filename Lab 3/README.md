# Lab 3 — Shell scripting

Bash scripts from the OS course. Run on any system with Bash (e.g. Linux or macOS).

## Scripts

| File | What it does |
|------|----------------|
| `swap.sh` | Reads two numbers and swaps them (no temp variable). |
| `prime.sh` | Reads a number and prints whether it is prime. |
| `odd_even.sh` | Reads a number and prints odd or even. |
| `leap.sh` | Reads a year and prints leap year or not (4/100/400 rules). |
| `area.sh` | Reads radius and prints circle area and circumference. |
| `files.sh` | Creates then deletes `file1.txt` … `file20.txt`. |
| `content.sh` | Compares `W1.txt` and `W2.txt` with `cmp` (identical or different). |
| `cprog.sh` | Asks for a folder name, finds all `.c` files, compiles and runs each. |

## Running

Make scripts executable if needed and run:

```bash
chmod +x script_name.sh
./script_name.sh
```

## Data files

- **`content.sh`** expects **`W1.txt`** and **`W2.txt`** in the same directory as the script. Create or copy these files in `Lab 3/` before running.
- **`cprog.sh`** uses **`filename.txt`** as an intermediate list of `.c` paths; it is created by the script.
- **`test/`** contains a sample **`test.c`**; you can point `cprog.sh` at `test` to try it.

## Folder layout

Scripts and the data files they use (e.g. `W1.txt`, `W2.txt`) live in this folder. The `test/` subfolder is only a sample C project for `cprog.sh`.
