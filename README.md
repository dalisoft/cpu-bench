# cpu-bench

CPU benchmark for measuring your machine performance easier without additional installation of benchmarking tool

## Sources

- <https://benchmarksgame-team.pages.debian.net/benchmarksgame/index.html>
- <https://www.youtube.com/watch?v=5ksXJGKF3Ug>

## Types

| Language | Filename                    | Type        | Argument   |
| -------- | --------------------------- | ----------- | ---------- |
| Python 3 | `./nbody-python3-1.py`      | Single-core | 50_000_000 |
| Python 3 | `./mandelbrot-python3-7.py` | Multi-core  | 50_000     |

## Results

| Machine            | Env       | Single-core time | Multi-core time |
| ------------------ | --------- | ---------------- | --------------- |
| MBP 16" 2021       | macOS 13  | ~161 sec         | ~446 sec        |
| MBP M1 2020        | macOS 13  | ~267 sec         | ~624 sec        |
| i9-9900K (4.8/4.6) | Win 11    | ~356 sec         | ~584 sec        |
| Xeon E5-2696 v3    | Ubuntu 22 | ~362 sec         | ~374 sec        |
| RPi 4B 4GB         | Debian 11 | ~1049 sec        | ~4336 sec       |

## Relative performance

| Machine            | Env       | Single-core | Multi-core |
| ------------------ | --------- | ----------- | ---------- |
| MBP 16" 2021       | macOS 13  | 100%        | 100%       |
| MBP M1 2020        | macOS 13  | 60%         | 71%        |
| i9-9900K (4.8/4.6) | Win 11    | 45%         | 76%        |
| Xeon E5-2696 v3    | Ubuntu 22 | 44%         | 119%       |
| RPi 4B 4GB         | Debian 11 | 15%         | 10%        |

## Preparation

### Ubuntu/Debian

```sh
sudo apt update -y && sudo apt upgrade -y
sudo apt install -y git python3
```

### macOS

```sh
brew update
brew install git python
```

### Windows 10 22H2+

```sh
winget install git python
# or
scoop install git python3 ps time
```

## Installation

```sh

git clone https://github.com/dalisoft/cpu-bench.git
cd cpu-bench
time python3 {FILENAME}
```
