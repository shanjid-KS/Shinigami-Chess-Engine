---

# Shinigami Chess Engine

![MIT License](https://img.shields.io/badge/license-MIT-green)
![Python](https://img.shields.io/badge/language-Python-blue)

**Shinigami V.1.15.8 – Gen 2 Edition**  
A professional, parallelized chess engine with advanced evaluation, dynamic learning, and a dash of attitude.

## Features

- **Full Tree Parallelization**: Multiprocessing for fast, deep analysis (Lazy SMP).
- **Enhanced Alpha-Beta Pruning**: Null move pruning, futility pruning, late move reductions, principal variation search (PVS), killer/history/SEE move ordering.
- **Deep Quiescence Search**: With tactical extension and threat detection.
- **Advanced Evaluation**: Piece-square tables, material, (optional) NNUE neural net, and Syzygy tablebases for endgames.
- **Dynamic Opening Book**: Learns from self-play and opponent games, includes pruning for quality.
- **Opponent Learning**: Updates book weights based on human play.
- **Self-Play & Training Module**: Generates games, (re)trains NNUE, and supports extensible feature engineering.
- **Profiling & Logging**: Search statistics, nodes/sec, transposition hits, cutoffs, and full cProfile dumps.
- **Trash Talk**: The engine taunts you as you play.
- **UCI Protocol**: Plug into Chess GUIs (Arena, CuteChess, etc.).
- **GUI & Console Modes**: Tkinter-based board or retro terminal mode.
- **Difficulty Modes**: From ‘easy’ to ‘Dialing Satan’s Number’ (with multi-step confirmation for extreme settings).
- **Placeholders for Policy Network & Feature Engineering**: Ready for future RL/Supervised move ordering and auto-tuning.

---

## Installation

1. **Clone the Repository**
    ```bash
    git clone https://github.com/Tonmoy-KS/Shinigami-Chess-Engine.git
    cd Shinigami-Chess-Engine
    ```

2. **Install Dependencies**
    ```bash
    pip install -r requirements.txt
    ```
    *Dependencies:*  
    `python-chess`, `numpy`, `scipy`, `torch`, `pillow`, `tkinter` (std on many systems)

3. **(Optional) Add Assets**
    - **NNUE**: Place `nnue_weights.bin` in the project root for neural evaluation
    - **Syzygy Tablebases**: Download and set the path in `ShinigamiConfig.SYZYGY_PATH`
    - **Opening Book**: (Polyglot) Place `book.bin` in the root if you want classic opening support

---

## Usage

**Play in Console (default):**
```bash
python Shinigami_engine.py
```
- Follow prompts, select your difficulty, and play as White or Black.

**GUI Mode:**
```bash
python Shinigami_engine.py --gui
```

**Self-Play & NNUE Training:**
```bash
python Shinigami_engine.py --self-play 100
```

**Control CPU Cores:**
```bash
python Shinigami_engine.py --cores 4
```

**Use as a UCI Engine (for Chess GUIs):**
- Launch: `python Shinigami_engine.py`
- Set up in your GUI as a UCI engine (see UCI protocol support below).

---

## Difficulty Modes

- **easy:** Entry-level, low search depth
- **medium:** Club level
- **hard:** Advanced/Expert level
- **god-of-death:** Grandmaster+
- **puzzle:** Solve preset tactical puzzles
- **masochist:** Insane depth, confirmation required!
- **dialing-satan-s-number:** Joke mode, extreme resources—multi-step confirmation for safety

---

## Major v1.15.8 Enhancements

- **Profiling & Logging**: cProfile integration; logs nodes searched, NPS, cutoffs, TT hits per depth.
- **Advanced Alpha-Beta Search**: Includes null move, futility and late move reduction pruning, plus PVS.
- **Dynamic Opening Book**: Learns and prunes from both self-play and human games; opponent move learning.
- **Opponent Learning**: Book is updated as you play, adapting to your style.
- **Move Ordering**: Killer moves, history heuristics, SEE for all moves, and placeholders for policy network ordering.
- **Policy Network Placeholders**: Hooks for RL/supervised move probability ordering.
- **Automated Feature Engineering Placeholder**: Ready for evolutionary/gradient tuning of evaluation params.
- **Syzygy Tablebase**: Deeper integration for accurate endgame scores.
- **Safety for Extreme Difficulties**: Multi-step confirmation prompts for “masochist” and “dialing-satan-s-number” modes.
- **GUI Improvements**: Now learns from your moves as you play in GUI mode.

---

## How to Read Logs and Profiling

- Logs are written to `shinigami_engine.log` (search stats, move picks, cutoffs, etc).
- Profiling output is in `shinigami_profile.prof`.  
  To visualize:  
  `pip install snakeviz`  
  `snakeviz shinigami_profile.prof`

---

## UCI Protocol Support

- Recognizes all standard UCI commands (`uci`, `isready`, `position`, `go`, etc.)
- Can be loaded into GUIs like Arena, Scid vs PC, CuteChess, etc.
- Accepts time controls via UCI commands

---

## License

MIT License.  
**Credit [Tonmoy-KS](https://github.com/Tonmoy-KS).**  
Do not claim as your own; fork, mod, and contribute instead!

---

## Contributing

Pull requests, feature ideas, and code reviews are welcome!  
For big changes, please open an issue first.

---

## Contact

- GitHub: [Tonmoy-KS](https://github.com/Tonmoy-KS)

---

*Happy reaping on the 64 squares!*

---