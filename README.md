---

# Shinigami Chess Engine

![MIT License](https://img.shields.io/badge/license-MIT-green)
![Python](https://img.shields.io/badge/language-Python-blue)
![Stars](https://img.shields.io/github/stars/Tonmoy-KS/Shinigami-Chess-Engine?style=social)

**Shinigami V.1.15.4 – Gen 2 Edition**  
A professional chess engine with full tree parallelization, advanced evaluation, and (optionally) NNUE neural nets.  
Inspired by Stockfish, but 100% original code by [Tonmoy-KS](https://github.com/Tonmoy-KS).  

> “Your moves are so predictable. I’m playing blindfolded.”  
> — *Shinigami Engine Trash Talk*

---

## Features

- **Full Tree Parallel Search** – Uses multiprocessing for fast, deep analysis.
- **Advanced Evaluation** – Piece-square tables, material, and optional Syzygy endgame tablebases.
- **NNUE (Neural Network Unified Evaluation)** – Pluggable HalfKAv2 neural net for positional understanding.
- **Opening Book** – Polyglot book support and self-play book trainer.
- **Self-Play & Training Module** – Generates games and retrains the NNUE.
- **GUI & Console Modes** – Tkinter board or retro text mode.
- **Difficulty Levels** – From ‘easy’ to ‘Dialing Satan’s Number’ (for masochists).
- **Trash Talk** – The engine will taunt you as you play.
- **UCI Protocol Support** – Plug into chess GUIs like Arena, CuteChess, etc.
- **MIT License** – Free to use, modify, and hack on (just credit the author).

---

## Installation

1. **Clone the Repo:**
    ```bash
    git clone https://github.com/Tonmoy-KS/Shinigami-Chess-Engine.git
    cd Shinigami-Chess-Engine
    ```

2. **Install Dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
    *(Main dependencies: python-chess, numpy, torch, scipy, Pillow)*

3. **(Optional) NNUE & Tablebases:**
    - Place your `nnue_weights.bin` (HalfKAv2) in the project root.
    - Download Syzygy Tablebases and set the path in `ShinigamiConfig.SYZYGY_PATH`.
    - Opening book: place `book.bin` in the root.

---

## Usage

**Basic Play (Console):**
```bash
python Shinigami_Engine
```
- Follow prompts to select difficulty and play as White or Black.

**GUI Mode:**
```bash
python Shinigami_Engine --gui
```

**Enable Self-Play / NNUE Training:**
```bash
python Shinigami_Engine --self-play 100
```

**Adjust CPU Cores:**
```bash
python Shinigami_Engine --cores 4
```

**UCI Protocol (for chess GUIs):**
- Run `python Shinigami_Engine` and use UCI commands as per your GUI.

---

## Difficulty Modes

- **easy:** Beginner, low search depth
- **medium:** Club level
- **hard:** Expert level
- **god-of-death:** Grandmaster+
- **puzzle:** Solve preset tactical puzzles
- **masochist:** Insane depth, for pain lovers
- **dialing-satan-s-number:** Joke mode. You were warned.

---

## Trash Talk Examples

- “Check! I’m carving your board like a Halloween pumpkin.”
- “Yoink! That piece is mine now.”
- “Invalid move! Did you borrow that from a 1000-rated game?”

---

## Architecture

- **Python 3** with heavy use of `python-chess`, multiprocessing, and PyTorch.
- Modular classes: Config, NNUE, Evaluator, Training, GUI, Engine.
- Transposition tables, piece-square tables, quiescence, alpha-beta, iterative deepening.
- UCI and GUI frontends.

---

## License

MIT License.  
**Credit [Tonmoy-KS](https://github.com/Tonmoy-KS).**  
Do not claim as your own; fork, mod, and contribute instead!

---

## Credits & Inspiration

- Inspired by Stockfish (but code is 100% self-written).
- Built by [Tonmoy-KS](https://github.com/Tonmoy-KS).

---

## Contributing

PRs/issues/suggestions are welcome!  
For big changes: open an issue first to discuss what you want to change.

---

## Contact

- GitHub: [Tonmoy-KS](https://github.com/Tonmoy-KS)

---

*Happy reaping on the 64 squares!*

---
