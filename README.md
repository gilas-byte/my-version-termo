# My Version of Termo

[![Licença: MIT](https://img.shields.io/badge/license-MIT-blue)](LICENSE) ![Linguagem: Python](https://img.shields.io/badge/language-Python-blue)

Clone em Python do [Termo](https://term.ooo/), a versão brasileira do Wordle. O objetivo é adivinhar uma palavra de cinco letras em português pelo terminal.

## O que faz

- **Demo original** (`termo_demo.py`): palavra fixa (`pilha`) e até cinco tentativas válidas.
- **Versão IA** (`termo_demo_ia.py`): palavra aleatória e até seis tentativas válidas. Apesar do nome, quem joga é você; não há um adversário automático.
- As duas versões usam a lista de palavras de `palavras_termo.py`.

As versões informam se cada letra está correta, deslocada ou ausente. São demos de terminal, sem interface gráfica, persistência de partidas ou jogador automático. A validação depende do dicionário local; a demo original verifica a presença das letras sem controlar quantas vezes cada uma aparece na palavra secreta.

## Estrutura do repositório

- `termo_demo.py`: demo com palavra fixa.
- `termo_demo_ia.py`: versão com sorteio de palavra e seis tentativas.
- `palavras_termo.py`: dicionário compartilhado pelas duas versões.
- `termo_demo.spec` e `termo_versao_ia.spec`: configurações de empacotamento com PyInstaller.
- `instructions.txt`: instruções de empacotamento para Windows, em inglês.

## Como rodar

Com Python 3 instalado e disponível como `python`, execute na pasta do projeto. Os scripts usam apenas a biblioteca padrão; não é necessário instalar dependências para jogar.

```bash
# Demo original
python termo_demo.py

# Versão IA
python termo_demo_ia.py
```

### Executáveis (opcional)

O repositório não inclui arquivos `.exe`. A pasta `dist/` é destinada às saídas locais de compilação e é ignorada pelo Git.

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

## Status

Estudo: projeto pessoal de aprendizado em Python, inspirado no [Termo](https://term.ooo/) de Fernando Serbetto.

## Licença

[MIT](LICENSE).
