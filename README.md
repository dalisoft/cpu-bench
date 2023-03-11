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

| Machine      | Single-core time | Multi-core time |
| ------------ | ---------------- | --------------- |
| MBP 16" 2021 | ~161 sec         | ~446 sec        |
| MBP M1 2020  | ~267 sec         | ~624 sec        |
| RPi 4B 4GB   | ~1049 sec        | -               |

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
