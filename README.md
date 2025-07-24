Here’s your revised README.md with the FAQ section incorporating your answers, plus the cosmic horror joke woven into the Difficulty Modes section!

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

---