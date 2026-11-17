# My Version of Termo

Clone em Python do [Termo](https://term.ooo/), a versão brasileira do Wordle. O objetivo é adivinhar uma palavra de cinco letras em português pelo terminal.

## Versões

- **Demo original** (`termo_demo.py`): palavra fixa (`pilha`) e até cinco tentativas válidas.
- **Versão IA** (`termo_demo_ia.py`): palavra aleatória e até seis tentativas válidas. Apesar do nome, quem joga é você; não há um adversário automático.
- As duas versões usam a lista de palavras de `palavras_termo.py`.

## Como rodar

Com Python 3 instalado, execute na pasta do projeto:

```bash
# Demo original
python termo_demo.py

# Versão IA
python termo_demo_ia.py
```

## Executáveis

Os arquivos `.exe` não ficam mais no repositório e serão publicados em **Releases**. A pasta `dist/` contém apenas saídas locais de compilação e é ignorada pelo Git.

Para gerar seus próprios executáveis, instale o [PyInstaller](https://pyinstaller.org/) e use os arquivos `.spec` existentes:

```bash
pip install pyinstaller

# Demo original
pyinstaller termo_demo.spec

# Versão IA
pyinstaller termo_versao_ia.spec
```

Para gerar `.exe`, rode esses comandos no Windows. Os resultados ficam em `dist/termo_demo.exe` e `dist/termo_versao_ia.exe`.

O arquivo [instructions.txt](instructions.txt) também traz comandos para Windows, partindo dos scripts `.py` com `--onefile --name`. Esses comandos usam nomes alternativos: `termo_beta_v1.exe` e `termo_beta_v1_ia.exe`.

As pastas `__pycache__/`, `build/`, `dist/` e `.venv/` são ignoradas pelo Git. Os arquivos `.spec` continuam versionados.

## Sobre

Projeto pessoal para aprender e se divertir, inspirado no [Termo](https://term.ooo/) de Fernando Serbetto.

## Licença

O repositório ainda não contém um arquivo `LICENSE`.
