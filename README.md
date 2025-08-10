---

# Shinigami Chess Engine (Latest, V.1.17.9 – Gen 2 Edition)

![MIT License](https://img.shields.io/badge/license-MIT-FF4136?labelColor=gray)
![Python](https://img.shields.io/badge/language-Python_3.8+-2ECC40?labelColor=gray)
![Creator](https://img.shields.io/badge/Creator_Name-Tonmoy_KS-0074D9?labelColor=gray)

**Shinigami V.1.17.9 – Gen 2 Edition (Latest)**  
_A professional chess engine with full tree parallelization, advanced NNUE evaluation, self-adapting features, enhanced puzzle system._

---

## 🚀 Latest Updates (V.1.17.9)
- **New Tactical Puzzle Generator:** Expanded database and improved task description for puzzle mode.  
- **Dynamic Opening Book Pruning:** Opening book now self-prunes weak lines, adapts even better to new opponents.  
- **Improved Evaluation:**  
  - Advanced king safety, pawn structure, mobility, and outpost detection.  
  - Enhanced rook/queen evaluation for open/semi-open files and connected pieces.  
- **NNUE & Policy Network:**  
  - Now supports full HalfKAv2 encoding for evaluation.  
  - CNN-based move-ordering with training from self-play is improved and weights auto-loaded.  
- **Genetic Feature Engineering:**  
  - Automated tuning for piece values and PSTs mid-game using DEAP.  
- **Trash Talk Engine:**  
  - Expanded, even more brutal/funny commentary (can be customized/disabled).  
- **Extreme Mode Safeguards:**  
  - “The Big Bang” mode is blocked by default, with triple-confirmation required on joke/extreme modes.  
- **Syzygy Tablebase:**  
  - Improved fallback and logging when tablebases not found.  
- **UCI Protocol:**  
  - Enhanced support for GUIs and time controls, automatic detection of options.
- **Multiprocessing:**  
  - Cross-platform safe, uses optimal pool sizes and dynamic chunking per system.
- **Voice Commentary:**  
  - TTS engine (pyttsx3) initialization improved; will warn/fallback if unavailable.
- **Logging:**  
  - Cleaner, more informative logs per game, search, and training.

---

## Features

- **Full Tree Parallelization:** Fast, multicore search for epic depth.
- **Advanced NNUE (HalfKAv2):** Modern neural evaluation (user-trainable).
- **CNN Policy Network:** Move ordering powered by a convolutional neural net.
- **Syzygy Tablebase Support:** Endgame perfection (≤7 pieces).
- **Genetic Feature Engineering:** DEAP-powered auto-tuning for piece values and tables.
- **Self-Play & Training:** Generates and learns from games, retrains NNUE and policy networks.
- **Dynamic Opening Book:** Adapts to self-play and opponent moves.
- **Opponent Learning:** Engine adapts to your style in real time.
- **Puzzle Generator:** Built-in tactical puzzles and board tasks.
- **GUI & Console:** Tkinter GUI (with mouse and text input) or classic terminal mode.
- **UCI Protocol:** Plug into chess GUIs (Arena, CuteChess, etc.).
- **Trash Talk Engine:** Witty, customizable, and (optionally) brutal.
- **Extreme Difficulty Modes:** From beginner to "The Big Bang" (with cosmic warnings...).

---

## Installation

**Clone the Repository:**
```bash
git clone https://github.com/Tonmoy-KS/Shinigami-Chess-Engine
cd Shinigami-Chess-Engine
```

**Install Dependencies:**
```bash
pip install -r requirements.txt
```
*Note: Ensure you have Python 3.8+.*

### Optional Assets
- **NNUE Weights:** Download `nnue_weights.bin` (HalfKAv2 compatible) and place in the project root or specify with `--nnue-file`.
- **Syzygy Tablebases:** Download and place .rtb files in `./tablebases` or specify path with `--syzygy-path`.
- **Polyglot Opening Book:** Place a `.bin` file in the project root or specify via command-line argument.

---

## Usage

**Console Mode:**
```bash
python3 Main_Code_1
```

**GUI Mode:**
```bash
python3 Main_Code_1 --gui
```

**Self-Play & Training:**
```bash
python3 Main_Code_1 --self-play 100
```

**Custom Paths & Cores:**
```bash
python3 Main_Code_1 --cores 4 --nnue-file /path/to/my_nnue.bin --syzygy-path /path/to/my_tablebases
```

**UCI Protocol (for chess GUIs):**
```bash
python3 Main_Code_1 --uci
```

---

## Logging

Search statistics, self-play games, and learning data are logged to `shinigami_engine.log`.

---

## Extreme Difficulty Modes Explained

The engine includes several extreme difficulty modes.

### Official
- **easy:** Beginner level.
- **medium:** Club-level player.
- **hard:** Strong player.
- **god-of-death:** Grandmaster+ level.
- **puzzle:** For solving tactical puzzles.

### Experimental/Jokes
- **masochist:** Insane mode requiring triple confirmation. May atomize or ionize your hardware.
- **dialing-satan-s-number:** Joke/extreme mode with a time control of "69 Eons." Triple confirmation required.
- **the-big-bang:** Experimental infinite depth/time mode, blocked for safety.

> **Cosmic Warning:**  
> Using the deepest modes may summon Outer Gods or turn your computer into a black hole. Use triple confirmation wisely!
---

### FAQ

1. **What makes Shinigami different from other chess engines?**  
   Full tree parallelization, advanced NNUE, CNN policy network, genetic feature engineering, and a unique "trash talk" engine and LLM-powered Explanations.

2. **How do I enable the "Trash Talk" feature?**  
   It's enabled by default! Prepare for witty, sometimes brutal, commentary during gameplay.

3. **What about the "The Big Bang" and "Dialing Satan's Number" modes? Are they real?**  
   Extreme, experimental modes. "The Big Bang" is blocked for safety. "Dialing Satan's Number" is a meme with massive time control.

4. **Does Shinigami learn/adapt openings from self-play or opponents?**  
   Absolutely, with dynamic pruning and statistics.

5. **How do I train/improve the Policy Network and NNUE modules?**  
   Use self-play, or provide your own datasets. See code for details.

6. **Can I customize/disable the engine's trash talk?**  
   Yes, modify the dictionary in the source or set it to empty.

7. **Are there known limitations or funny side effects using Syzygy or deepest modes?**  
   "Your Firmware may summon Outer Gods if you use the Deepest Search modes."

8. **Is Shinigami UCI-compliant for GUIs?**  
   Yes, with enhanced and auto-detected options.

9. **Can users contribute their own neural weights, feature sets, or puzzles?**  
   Absolutely, contributions are welcome!

10. **What if the engine crashes or hardware is "atomized" by extreme settings?**  
    Read the triple-confirmation warnings. Proceed at your own risk!

11. **Recommended system requirements for extreme modes?**  
    Use first five modes for stability. Experimental/joke modes are for memes only.

12. **How does Shinigami handle different time controls and optimize for each?**  
    Time controls are adjustable in code and via command-line.

13. **Can users customize playing style (aggressive, positional)?**  
    Planned for future update!

14. **Key differences in "Gen 2 Edition"?**  
    Major improvements after V.1.10.0; see "Latest Updates" above.

15. **Roadmap for future development?**  
    Yes, but not public.

---

## License

**License:** MIT License  
**Credit:** Tonmoy-KS  
Do not claim as your own; fork, mod, and contribute instead!

---

## Contributing

Pull requests, feature ideas, and code reviews are welcome! For major contributions, open an issue first.

---

## Contact

GitHub: [Tonmoy-KS](https://github.com/Tonmoy-KS)

---

*Happy reaping in 64 squares!* — bye

---