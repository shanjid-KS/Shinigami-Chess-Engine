---

## README.md

```markdown
#### Shinigami-Chess-Engine

**Shinigami Chess Engine** is a professional chess engine with full tree parallelization, developed by Tonmoy-KS.

> **Note:**  
> This engine is **inspired by Stockfish**, but all code is original and self-written by @Tonmoy-KS.

---

#### Status

- ⚠️ The engine may still have some syntax and other errors.  
- I am actively fixing them and will provide a fully fixed version soon.
- You can find the current code in the `Main_Code_1` section.

---

## Dependencies

To run Shinigami Chess Engine, install the following dependencies.

| Dependency         | Version    | Purpose                        | Installation Command                                      | Platforms         |
|--------------------|------------|--------------------------------|-----------------------------------------------------------|-------------------|
| `python-chess`     | >=0.31.4   | Chess logic & UCI protocol     | `pip install python-chess`                                | Desktop, Android  |
| `numpy`            | >=1.21.0   | NNUE computations              | `pip install numpy`                                       | Desktop, Android  |
| `scipy`            | >=1.7.0    | Sparse matrix for NNUE         | `pip install scipy` <br> or <br> `pip install --index-url https://www.piwheels.org/simple scipy` (Android) | Desktop, Android  |
| `argparse`         | Std Library| CLI arguments                  | Included with Python                                      | Desktop, Android  |
| `logging`          | Std Library| Logging                        | Included with Python                                      | Desktop, Android  |
| `multiprocessing`  | Std Library| Parallel search                | Included with Python                                      | Desktop, Android (limited) |

### Optional Dependencies

| Dependency           | Purpose                    | Setup                                                                                   | Platforms         |
|----------------------|----------------------------|-----------------------------------------------------------------------------------------|-------------------|
| NNUE Weights         | Advanced evaluation        | Download or train, place in `./` (Desktop) or `/storage/emulated/0/shinigami/` (Android)| Desktop, Android  |
| Polyglot Opening Book| Opening moves database     | Download from [Lichess](https://database.lichess.org/#openings)                         | Desktop, Android  |
| Syzygy Tablebases    | Endgame accuracy           | Download from [Syzygy](http://tablebase.sesse.net/) and place in `tablebases/`          | Desktop, Android  |

### Training (Optional)

| Dependency | Version | Purpose         | Installation         | Platforms      |
|------------|---------|----------------|----------------------|----------------|
| `torch`    | >=1.9.0 | NNUE training  | `pip install torch`  | Desktop only   |
| Chess Dataset | N/A  | Training data  | Download from [Lichess Elite Database](https://database.lichess.org/) | Desktop |

---

## Installation

1. **Install Python**  
   - Desktop: [Download Python 3.8+](https://www.python.org/downloads/)
   - Android: Install Pydroid 3 from Google Play Store

2. **Install core dependencies:**
   ```sh
   pip install python-chess numpy scipy
   ```
---

## License

This project is licensed under the MIT License.  
If you use or modify this engine, **credit Tonmoy-KS as the original author**.  
Do not claim this project as your own.

---

### Acknowledgement

- Inspired by [Stockfish](https://stockfishchess.org/), but all code is original.

---

### Contact

For issues or contributions, please open an issue or pull request on GitHub.

---

*Last updated: June 27 2025*
```