# cpu-bench

## Sources
- https://benchmarksgame-team.pages.debian.net/benchmarksgame/index.html
- https://www.youtube.com/watch?v=5ksXJGKF3Ug

## Types

| Language | Filename                    | Type        |
| -------- | --------------------------- | ----------- |
| Python 3 | `./nbody-python3-1.py`      | Single-core |
| Python 3 | `./mandelbrot-python3-7.py` | Multi-core  |

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
