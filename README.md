
---

# Shinigami Chess Engine

![MIT License](https://img.shields.io/badge/license-MIT-green)
![Python](https://img.shields.io/badge/language-Python-blue)

**Shinigami V.1.16.0 – Gen 2 Edition**  
A professional, fully parallelized chess engine with advanced NNUE neural evaluation, genetic feature optimization, dynamic learning, and a dash of trash talk.

---

## Features

- **Full Tree Parallelization:** Multiprocessing for rapid, deep search.
- **Advanced Alpha-Beta Pruning:** Principal Variation Search (PVS), null-move pruning, futility pruning, late move reductions (LMR), and killer/history move heuristics.
- **Policy Network Integration:** Neural network (PyTorch) suggests move probabilities to enhance move ordering.
- **Dynamic NNUE Support:** Modern neural evaluation (toggleable, PyTorch required).
- **Self-Play & Training Module:** Generates training data, retrains NNUE, and learns from real games.
- **Genetic Feature Engineering:** Experimental auto-tuning for evaluation parameters using genetic algorithms.
- **Dynamic Opening Book:** Learns from both self-play and human games, prunes low-performing lines.
- **Opponent Learning:** Engine adapts its opening repertoire based on your moves.
- **Syzygy Tablebase Integration:** Accurate endgame analysis for positions with ≤7 pieces.
- **Profiling & Logging:** Search stats, profiling output for optimization.
- **GUI & Console Modes:** Play via Tkinter GUI or terminal.
- **UCI Protocol:** Compatible with modern chess GUIs.
- **Difficulty Modes:** From casual to “Dialing Satan’s Number” (with confirmation).
- **Trash Talk:** Expect attitude, not mercy.

---

## Installation

1. **Clone the Repository**
    ```bash
    git clone https://github.com/Tonmoy-KS/Shinigami-Chess-Engine.git
    cd Shinigami-Chess-Engine
    ```

2. **Install Dependencies**
    ```bash
    pip install python-chess numpy scipy torch pillow
    ```
    GUI requires Tkinter (bundled on most systems).

3. **Optional: Assets**
    - **NNUE:** Place `nnue_weights.bin` in the project root (for neural evaluation).
    - **Syzygy Tablebases:** Download and set the path in `ShinigamiConfig.SYZYGY_PATH`.
    - **Opening Book:** (Polyglot) Place `book.bin` in the root if available.

---

## Usage

**Console Mode (default):**
```bash
python Shinigami_engine.py
```
- Select difficulty and play as White or Black.

**GUI Mode:**
```bash
python Shinigami_engine.py --gui
```

**Self-Play / NNUE Training:**
```bash
python Shinigami_engine.py --self-play 100
```

**Control CPU Cores:**
```bash
python Shinigami_engine.py --cores 4
```

**UCI Protocol (for GUIs):**
- Load as a UCI engine in Arena, Scid vs PC, CuteChess, etc.

---

## Difficulty Modes

- **easy:** Beginner
- **medium:** Club level
- **hard:** Strong
- **god-of-death:** Grandmaster+
- **puzzle:** Solve tactical puzzles
- **masochist:** Insane (confirmation required)
- **dialing-satan-s-number:** Joke/extreme mode (triple confirmation required)

---

## Major v1.16.0 Enhancements

- **Policy Network:** Neural move-ordering for deeper search efficiency.
- **Genetic Feature Engineering:** Experimental auto-tuning for piece values and PSTs.
- **Pruned, Normalized Opening Book:** Keeps only best lines, adapts from both self-play and your games.
- **Better Learning:** Tracks opponent strength, prunes weak openings faster.
- **Profiling:** cProfile dumps to `shinigami_profile.prof` (see with `snakeviz shinigami_profile.prof`).
- **Expanded Trash Talk:** Witty responses for every situation.

---

## Logging & Profiling

- Logs: `shinigami_engine.log` (search stats, learning, pruning).
- Profiling: `shinigami_profile.prof` (visualize with [SnakeViz](https://jiffyclub.github.io/snakeviz/)).

---

## License

MIT License.  
**Credit [Tonmoy-KS](https://github.com/Tonmoy-KS).**  
Do not claim as your own; fork, mod, and contribute instead!

---

## Contributing

PRs, feature ideas, and code reviews are welcome! For major contributions, open an issue first.

---

## Contact

- GitHub: [Tonmoy-KS](https://github.com/Tonmoy-KS)

---

*Happy reaping on the 64 squares!*

---