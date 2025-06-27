# Shinigami-Chess-Engine
This Repository is Exclusive to the Shinigami Engine. **Shinigami Chess Engine**: this is a chess engine with full tree parallelization, made by Tonmoy-KS. This engine is Inspired by Stockfish but the Code is All Self-written original by Tonmoy-KS. 

# README.md
this engine still has some Syntax and other errors, i am fixing them. i will provide the full fixed code later. you can find the current code in the "Main_Code_1" section. 

## Dependencies

To run the Shinigami Chess Engine, install the following dependencies. The requirements vary slightly depending on your platform (Desktop or Android).

### Core Dependencies
| Dependency | Version | Purpose | Installation | Platforms |
|------------|---------|---------|--------------|-----------|
| `python-chess` | >=0.31.4 | Chess board logic and UCI protocol | `pip install python-chess` | Desktop, Android |
| `numpy` | >=1.21.0 | Numerical computations for NNUE | `pip install numpy` | Desktop, Android |
| `scipy` | >=1.7.0 | Sparse matrix operations for NNUE | `pip install scipy` or `pip install --index-url https://www.piwheels.org/simple scipy` (Android) | Desktop, Android |
| `argparse` | Standard Library | Command-line argument parsing | Included with Python | Desktop, Android |
| `logging` | Standard Library | Logging game events | Included with Python | Desktop, Android |
| `multiprocessing` | Standard Library | Parallel search | Included with Python | Desktop, Android (limited) |

### Optional Dependencies
| Dependency | Purpose | Setup | Platforms |
|------------|---------|-------|-----------|
| NNUE Weights (`nnue_weights.bin`) | Advanced position evaluation | Generate with `train_nnue.py` or download pre-trained file. Place in `./` (Desktop) or `/storage/emulated/0/shinigami/` (Android) | Desktop, Android |
| Polyglot Opening Book (`book.bin`) | Improved opening play | Download from [Lichess](https://database.lichess.org/#openings). Place in `./` or `/storage/emulated/0/shinigami/` | Desktop, Android |
| Syzygy Tablebases | Precise endgame play | Download 3-4 piece tablebases from [Syzygy](http://tablebase.sesse.net/). Place in `tablebases/` | Desktop (full set), Android (minimal set) |

### Training Dependencies (Optional)
| Dependency | Version | Purpose | Installation | Platforms |
|------------|---------|---------|--------------|-----------|
| `torch` | >=1.9.0 | NNUE training | `pip install torch` | Desktop (not recommended for Android) |
| Chess Dataset | N/A | Training data | Generate with Stockfish or download from [Lichess Elite Database](https://database.lichess.org/) | Desktop |

### Installation Instructions
1. **Install Python**:
   - Desktop: Python 3.8+ from [python.org](https://www.python.org/downloads/).
   - Android: Install Pydroid 3 from the Google Play Store.

2. **Install Core Dependencies**:
   ```bash
   pip install python-chess numpy scipy