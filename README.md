---

# Shinigami Chess Engine

![MIT License](https://img.shields.io/badge/license-MIT-red)
![Python](https://img.shields.io/badge/language-Python_3.8+-green)
![Creator](https://img.shields.io/badge/Creator_Name-Tonmoy_KS-Blue)

**Shinigami V.1.16.9 – Gen 2 Edition**  
_A professional chess engine with full tree parallelization, advanced NNUE evaluation, self-adapting features, and a cosmic sense of humor._

---
### Features:

 * Full Tree Parallelization: Fast, multicore search for epic depth.
 * Advanced NNUE (HalfKAv2): Modern neural evaluation (user-trainable).
 * CNN Policy Network: Move ordering powered by a convolutional neural net.
 * Syzygy Tablebase Support: Endgame perfection (≤7 pieces).
 * Genetic Feature Engineering: DEAP-powered auto-tuning for piece values and tables.
 * Self-Play & Training: Generates and learns from games, retrains NNUE and policy networks.
 * Dynamic Opening Book: Adapts to self-play and opponent moves.
 * Opponent Learning: Engine adapts to your style in real time.
 * Puzzle Generator: Built-in tactical puzzles and board tasks.
 * GUI & Console: Tkinter GUI (with mouse and text input) or classic terminal mode.
 * UCI Protocol: Plug into chess GUIs (Arena, CuteChess, etc.).
 * Trash Talk Engine: Witty, customizable, and (optionally) brutal.
 * Extreme Difficulty Modes: From beginner to "The Big Bang" (with cosmic warnings...).

---

### Installation

Clone the Repository using:
```Clone the Repository
git clone https://github.com/Tonmoy-KS/Shinigami
cd Shinigami
```

and then Install the Dependencies using:
```Install Dependencies
pip install -r requirements.txt
```
   Note: Ensure you have Python 3.8+.

#### Optional Assets

   * NNUE Weights: Download nnue_weights.bin (HalfKAv2 compatible) and place it in the project root or specify the path using `--nnue-file`.

   * Syzygy Tablebases: Download and place .rtb files in ./tablebases or specify the path using --syzygy-path.
   * Polyglot Opening Book: Place a .bin file in the project root or specify it via a command-line argument.
Usage

---
#### Startup Tutorial

```Console Mode
python3 shinigami_Engine.py
```

```GUI Mode
python3 shinigami_Engine.py --gui
```

```Self-Play & Training
python3 shinigami_Engine.py --self-play 100
python3 shinigami_Engine.py --train-nnue
python3 shinigami_Engine.py --auto-tune
```
```Custom Paths & Cores
python3 shinigami_Engine.py --cores 4 --nnue-file /path/to/my_nnue.bin --syzygy-path /path/to/my_tablebases
```
---

### Logging

Search statistics, self-play games, and learning data are logged to shinigami_engine.log.

---

### Extreme Difficulty Modes Explained

The engine includes several extreme difficulty modes.

#### Official: 
 * easy: Beginner level.
 * medium: Club-level player.
 * hard: Strong player.
 * god-of-death: Grandmaster+ level.
 * puzzle: For solving tactical puzzles.

#### Experimental/Jokes
 * masochist: An insane mode requiring triple confirmation for those who enjoy pain. Using this or "Dialing Satan's Number" mode may atomize or ionize your hardware.
 * dialing-satan-s-number: A joke/extreme mode, also requiring triple confirmation. It comes with a time control of "69 Eons."
 * the-big-bang: An experimental infinite depth and time mode that is blocked for safety due to its extreme nature.

---

### FAQ

1. What makes Shinigami different from other chess engines?
A: Shinigami features full tree parallelization, advanced NNUE, CNN policy network, genetic feature engineering, and a unique "trash talk" engine.

2. How do I enable the "Trash Talk" feature?
A: It's enabled by default! Prepare for witty, sometimes brutal, commentary during gameplay.

3. What about the "The Big Bang" and "Dialing Satan's Number" modes? Are they real?
A: These are extreme, experimental modes. "The Big Bang" offers infinite depth and time, but it's blocked for safety. "Dialing Satan's Number" has a intentional 69 Eons long time control. They exist for fun, but use the triple confirmation ritual wisely; Shinigami may Force your firmware to summon Cthulhu,so the Engine can have a Buddy to drink tea.

4. Is there support for custom opening books, and how does Shinigami learn/adapt openings from self-play or opponents?
A: Yes, it absolutely does.

5. What's the best way to train or improve the Policy Network and NNUE modules?
A: You can learn it from someone else, and there are instructions.

6. How does the engine's trash talk feature work, and can it be customized or disabled?
A: Yes, it can be customized, and you can disable it by wiping the entire module's dictionary.

7. Are there known limitations or funny side effects when using Syzygy tablebases or the deepest search modes?
A: The only answer is 'Your Firmware may summon Outer Gods if you use the Deepest Search modes'.

8. Is Shinigami UCI-compliant for easy integration with chess GUIs?
A: It has UCI protocols.

9. Can users contribute their own neural weights, feature sets, or puzzles?
A: Absolutely. Thanks for the help!

10. What should users do if the engine crashes or their hardware is "atomized" by extreme settings?
A: Ahem, you should've read what you agreed to when the 3 Confirmation Ritual was happening.

11. What are the recommended system requirements for running Shinigami, especially for the more extreme difficulty modes?
A: The difficulty modes from 6-8 are purely for memes. I heavily recommend you don't use those and use the first 5.

12. How does Shinigami handle different time controls (e.g., blitz, rapid, classical), and are there specific settings to optimize performance for each?
A: Yes, you can change the time controls to the specific mode in the source code.

13. Can users customize the engine's playing style beyond just difficulty settings (e.g., more aggressive, positional)?
A: Currently no, but I will soon add an option.

14. What are the key differences or improvements in the "Gen 2 Edition" compared to previous generations of Shinigami?
A: The Gen 2 started after V.1.10.0, after the Beta Testing phase was over.

15. Is there a roadmap for future development or upcoming features for Shinigami?
A: I have an outline planning system for my engine, which I cannot publicly share.
License

---
#### Details
License: MIT License
Credit: Tonmoy-KS.
Do not claim as your own; fork, mod, and contribute instead!

---

### Contributing
Pull requests, feature ideas, and code reviews are welcome! For major contributions, open an issue first.

---

#### Contact
GitHub: Tonmoy-KS

---

*happy reaping in 64 squares!* — bye

---



