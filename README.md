# My Version of Termo 🟩

A Python-based clone of [Termo](https://term.ooo/) — the Brazilian version of Wordle. Guess the 5-letter Portuguese word in 6 attempts!

## Features

- **Standard mode** (`termo_demo.py`) — classic Termo gameplay in the terminal
- **AI mode** (`termo_demo_ia.py`) — an AI opponent that tries to guess the word automatically
- Word list from `palavras_termo.py`

## How to Run

Make sure you have Python 3 installed, then:

```bash
# Standard mode
python termo_demo.py

# AI mode
python termo_demo_ia.py
```

## Build Executable

You can package the game into a standalone executable using [PyInstaller](https://pyinstaller.org/):

```bash
pip install pyinstaller

# Standard version
pyinstaller --onefile termo_demo.py

# AI version
pyinstaller --onefile termo_demo_ia.py
```

The executables will be generated in the `dist/` folder.

## About

This is a personal project built for fun and learning. Inspired by the original [Termo](https://term.ooo/) by Fernando Serbetto.

## License

See [LICENSE](LICENSE) for details.
