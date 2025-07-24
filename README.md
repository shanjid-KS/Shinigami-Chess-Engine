---

# Shinigami Chess Engine

![MIT License](https://img.shields.io/badge/license-MIT-red)
![Python](https://img.shields.io/badge/language-Python_3-green)
![Creator](https://img.shields.io/badge/Creator_Name-Tonmoy_KS-blue)

**Shinigami V.1.16.7 – Gen 2 Edition**  
_A professional chess engine with full tree parallelization, advanced NNUE evaluation, self-adapting features, and a cosmic sense of humor._

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
- **the-big-bang:** ∞ depth & ∞ time ("No engine nor hardware known to man can survive this. Selection blocked for your own safety.")

> ⚠️ **Cosmic Warning:**  
> If your game reaches a 7-piece endgame, it's probably already over.  
> If you complete the **Triple Confirmation Ritual** for "Masochist" or "Dialing Satan's Number" mode, your hardware may be atomized, ionized, and transformed into a singularity orbiting Ton 618.  
> Try to select "The Big Bang" and you’ll just get roasted by the engine itself, or risk summoning Entropy-Kun.

---

## Minor v1.16.7 Changes

- **New 8th Difficulty:** "The Big Bang" (infinite time/depth, but blocked for sanity & comedy).
- **Optimizations:** Faster search, deeper analysis, snappier GUI.
- **More Trash Talk:** Especially for cosmic-scale mistakes.
- **Enhanced Safety:** "The Big Bang" can’t be enabled, but you’ll get a universe-ending message if you try.

---

## Logging & Profiling

- Logs: `shinigami_engine.log` (search stats, learning, pruning).
- Profiling: `shinigami_profile.prof` (visualize with [SnakeViz](https://jiffyclub.github.io/snakeviz/)).

---

## FAQ

**1. What is the main strength or unique selling point of Shinigami Chess Engine compared to other engines?**  
A: My Engine is similar to AlphaZero, it has Automated Systems that Change its PSTs, Piece Values and Adapt to the Opponent mid-game.

**2. How does Shinigami’s NNUE implementation differ from Stockfish’s or other engines?**  
A: I can't fully answer that because the NNUE needs to be Trained by the User themselves.

**3. What hardware specs are recommended for running the engine at extreme settings (e.g., “masochist” or “dialing-satan-s-number”)?**  
A: You'll either need a Quantum Supercomputer with a Black hole Penson Swarm Plugged in or a Death Wish.

**4. Is there support for custom opening books, and how does Shinigami learn/adapt openings from self-play or opponents?**  
A: Yes, it Absolutely does.

**5. What’s the best way to train or improve the Policy Network and NNUE modules?**  
A: You can learn it from Someone Else. 

**6. How does the engine’s trash talk feature work, and can it be customized or disabled?**  
A: Yes, it can be Customized and you can disable it by wiping the entire module's Dictionary.

**7. Are there known limitations or funny side effects when using Syzygy tablebases or the deepest search modes?**  
A: The only answer is `Your Firmware may summon Outer Gods if you use the Deepest Search modes`.

**8. Is Shinigami UCI-compliant for easy integration with chess GUIs?**  
A: It has UCI protocols.

**9. Can users contribute their own neural weights, feature sets, or puzzles?**  
A: Absolutely. thanks for the Help!

**10. What should users do if the engine crashes or their hardware is “atomized” by extreme settings?**  
A: Ahem, you should've read what you agreed to when the 3 Confirmation Ritual was happening.

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

—
