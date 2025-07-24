---

# Shinigami Chess Engine

![MIT License](https://img.shields.io/badge/license-MIT-green)
![Python](https://img.shields.io/badge/language-Python-blue)

**Shinigami V.1.16.6 – Gen 2 Edition**  
_A professional chess engine with advanced NNUE neural evaluation, full tree parallelization, genetic feature optimization, and a dash of trash talk._

---

## Features

- **Full Tree Parallelization:** Multiprocessing for deep, fast search.
- **Advanced NNUE (HalfKAv2):** Modern neural network evaluation, enabled by default.
- **CNN-Based Policy Network:** Move ordering powered by a convolutional neural net.
- **Syzygy Tablebase Integration:** Fast, accurate endgame scoring (≤7 pieces).
- **Genetic Feature Engineering:** Auto-tunes evaluation parameters with DEAP (`pip install deap`).
- **Self-Play & Training:** Generates and learns from games, retrains both NNUE and policy networks.
- **Dynamic Opening Book:** Tracks win/loss/draw statistics, prunes weak lines, adapts from your play.
- **Opponent Learning:** Engine adapts its book based on your moves and strength.
- **Puzzle Generator:** Built-in tactical puzzles and board tasks.
- **GUI & Console Modes:** Tkinter GUI with mouse and text input, or classic terminal mode.
- **UCI Protocol:** Plug into chess GUIs (Arena, CuteChess, etc.).
- **Difficulty Modes:** From beginner to "Dialing Satan's Number" (with confirmation).
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
    pip install python-chess numpy scipy torch pillow deap
    ```
    GUI requires Tkinter (bundled on most systems).

3. **Optional: Assets**
    - **NNUE:** Place `nnue_weights.bin` in the project root (or use `--nnue-file`).
    - **Syzygy Tablebases:** Download and set the path in `--syzygy-path` or environment variable.
    - **Opening Book:** (Polyglot) Place `book.bin` in the root if available.

---

## Usage

**Console Mode (default):**
```bash
python Shinigami_Engine.py
```
- Select difficulty, play as White or Black.

**GUI Mode:**
```bash
python Shinigami_Engine.py --gui
```

**Self-Play, NNUE & Policy Training:**
```bash
python Shinigami_Engine.py --self-play 100
```

**Custom NNUE/Tablebase Paths:**
```bash
python Shinigami_Engine.py --nnue-file ./weights.bin --syzygy-path ./tablebases
```

**Control CPU Cores:**
```bash
python Shinigami_Engine.py --cores 4
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
- **masochist:** Insane (triple confirmation required!)
- **dialing-satan-s-number:** Joke/extreme mode (triple confirmation required!)

> ⚠️ **Cosmic Warning:**  
> If your game reaches a 7-piece endgame, it's probably already over.  
> But if you complete the **Triple Confirmation Ritual** for "Masochist" or "Dialing Satan's Number" mode...
>
> Your hardware may be atomized, ionized, and transformed into a singularity orbiting Ton 618.  
> Cthulhu might show up for tea.  
> Proceed at your own risk—and keep your sanity and CPU cooling handy.

---

## Major v1.16.6 Enhancements

- **CNN Policy Network:** Convolutional neural net for move ordering (trained from self-play).
- **NNUE HalfKAv2:** Expanded feature set (98304 inputs, clipped ReLU).
- **Improved Opening Book:** Tracks win/loss/draw rates, prunes weak openings, adapts to player strength.
- **Self-Play Parallelization:** Fast game generation using multiprocessing.
- **GUI:** Tkinter board with mouse and text input, highlights legal moves.
- **Search Interruption:** UCI "stop" command halts search gracefully.
- **Dynamic Time Controls:** Time allocation scales with position complexity.
- **Enhanced Trash Talk:** Witty responses for every situation.

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

Pull requests, feature ideas, and code reviews are welcome!  
For major contributions, open an issue first.

---

## Contact

- GitHub: [Tonmoy-KS](https://github.com/Tonmoy-KS)

---

*Happy reaping on the 64 squares!*

---
