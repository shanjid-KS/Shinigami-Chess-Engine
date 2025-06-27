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

## Android Notes

- **File Storage**:
  - Place all engine resources (`nnue_weights.bin`, `book.bin`, tablebases, `shinigami_engine.log`) in `/storage/emulated/0/shinigami/`.
  - Create the directory if it doesn’t exist:
    ```sh
    mkdir /storage/emulated/0/shinigami
    ```
  - Ensure Pydroid 3 has storage permissions (grant via Android settings).
  - Alternatively, files can be placed in Pydroid 3’s internal storage (`/data/data/ru.iiec.pydroid3/files/`), but `/storage/emulated/0/shinigami/` is recommended for accessibility.

- **Performance**:
  - Use "easy" or "medium" modes (depth ≤ 8) to avoid slowdowns on mobile devices.
  - Multiprocessing is limited to 1 core by default to prevent crashes. Use `--cores 1` when running:
    ```sh
    python shinigami.py --cores 1
    ```

- **Dependencies**:
  - Install via Pydroid 3’s terminal:
    ```sh
    pip install python-chess numpy scipy
    ```
  - If `scipy` fails, use:
    ```sh
    pip install --index-url https://www.piwheels.org/simple scipy
    ```

- **Running the Engine**:
  - Console mode: Run `python shinigami.py` in Pydroid 3 and select a difficulty.
  - UCI mode: Use a chess app like DroidFish, running:
    ```sh
    python shinigami.py --uci
    ```

- **Troubleshooting**:
  - **Missing Files**: Ensure `nnue_weights.bin` and `book.bin` are in `/storage/emulated/0/shinigami/`. Download from [GitHub Releases](https://github.com/Tonmoy-KS/Shinigami-Chess-Engine/releases).
  - **Permission Errors**: Grant storage permissions in Android settings.
  - **Crashes**: Reduce NNUE size (edit `AdvancedNNUEEvaluator.hidden_size1` to 128) or disable tablebases.
  - Check `shinigami_engine.log` in `/storage/emulated/0/shinigami/` or console output for errors.

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