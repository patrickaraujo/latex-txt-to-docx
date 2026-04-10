# latex-txt-to-docx

Jupyter Notebook tool that converts `.txt` files containing LaTeX formulas into formatted `.docx` documents. Developed for academic content preparation.

*Ferramenta em Jupyter Notebook para conversão de arquivos `.txt` contendo fórmulas LaTeX em documentos `.docx` formatados. Desenvolvida para produção de material didático.*

---

## 🇬🇧 English

### Overview

This notebook reads a text file (or a string defined directly in the code) containing LaTeX formulas and produces a clean `.docx` document with the following formatting rules:

- **LaTeX formulas** (`$...$` and `$$...$$`) → rendered as raw code in a separate, centered paragraph using a monospaced font (Courier New)
- **Quoted text** (`"..."` and `'...'`) → converted to italic
- **Regular text** → rendered in the default font (Calibri)
- **Soft line breaks** (single `\n`) → treated as continuation of the same paragraph
- **Paragraph breaks** (double `\n\n`) → preserved as new paragraphs
- **Escaped characters** (`\"`, `\'`) and **formatting asterisks** (`*text*`) → automatically removed

### Features

- **Two input modes:** read from a `.txt` file or use a string directly in the code
- **Automatic text cleaning:** removes soft wraps, escape characters, and markdown-style asterisks
- **Preview step:** prints the generated document structure for quick verification
- **Customizable:** fonts, sizes, and colors can be adjusted in the configuration cell

### Requirements

- Python 3.8+
- `python-docx`
- Jupyter Notebook or JupyterLab

### Usage

1. Open `formatar_latex_para_docx.ipynb` in Jupyter
2. In cell 2, set `MODO = "arquivo"` to read from a file, or `MODO = "string"` to use inline text
3. Adjust `ARQUIVO_ENTRADA`, `ARQUIVO_SAIDA`, or `TEXTO_DIRETO` as needed
4. Run all cells — the `.docx` file will be generated in the current directory

### Example

**Input (`.txt`):**
```
The permutation formula is $P_{n} = n!$, where $n$ is the number of elements.
Consider the word "CASA" — it has 4 letters.
```

**Output (`.docx`):**
- Paragraph: "The permutation formula is"
- Centered formula (monospace): `$P_{n} = n!$`
- Paragraph: ", where"
- Centered formula (monospace): `$n$`
- Paragraph: "is the number of elements. Consider the word *CASA* — it has 4 letters." (with "CASA" in italic)

---

## 🇧🇷 Português

### Visão geral

Este notebook lê um arquivo de texto (ou uma string definida diretamente no código) contendo fórmulas LaTeX e gera um documento `.docx` formatado com as seguintes regras:

- **Fórmulas LaTeX** (`$...$` e `$$...$$`) → exibidas como código bruto em parágrafo separado, centralizado, com fonte monoespaçada (Courier New)
- **Trechos entre aspas** (`"..."` e `'...'`) → convertidos para itálico
- **Texto comum** → fonte padrão (Calibri)
- **Quebras de linha simples** (`\n`) → tratadas como continuação do mesmo parágrafo
- **Quebras de parágrafo** (`\n\n`) → preservadas como novos parágrafos
- **Caracteres escapados** (`\"`, `\'`) e **asteriscos de formatação** (`*texto*`) → removidos automaticamente

### Funcionalidades

- **Dois modos de entrada:** leitura de um arquivo `.txt` ou uso direto de string no código
- **Limpeza automática:** remove soft wraps, caracteres escapados e asteriscos de formatação
- **Pré-visualização:** exibe a estrutura do documento gerado para conferência rápida
- **Personalização:** fontes, tamanhos e cores podem ser ajustados na célula de configuração

### Requisitos

- Python 3.8+
- `python-docx`
- Jupyter Notebook ou JupyterLab

### Como usar

1. Abra `formatar_latex_para_docx.ipynb` no Jupyter
2. Na célula 2, defina `MODO = "arquivo"` para ler de um arquivo, ou `MODO = "string"` para usar texto direto no código
3. Ajuste `ARQUIVO_ENTRADA`, `ARQUIVO_SAIDA` ou `TEXTO_DIRETO` conforme necessário
4. Execute todas as células — o arquivo `.docx` será gerado no diretório atual

### Exemplo

**Entrada (`.txt`):**
```
A fórmula da permutação é $P_{n} = n!$, onde $n$ é o número de elementos.
Considere a palavra "CASA" — ela possui 4 letras.
```

**Saída (`.docx`):**
- Parágrafo: "A fórmula da permutação é"
- Fórmula centralizada (monoespaçada): `$P_{n} = n!$`
- Parágrafo: ", onde"
- Fórmula centralizada (monoespaçada): `$n$`
- Parágrafo: "é o número de elementos. Considere a palavra *CASA* — ela possui 4 letras." (com "CASA" em itálico)

---

## 📁 Project structure / Estrutura do projeto

```
latex-txt-to-docx/
├── formatar_latex_para_docx.ipynb   # Main notebook / Notebook principal
├── exemplo.txt                      # Sample input file / Arquivo de exemplo
├── saida.docx                       # Generated output / Saída gerada
└── README.md
```

## 📄 License / Licença

MIT License — feel free to use, modify, and share.

*Licença MIT — sinta-se à vontade para usar, modificar e compartilhar.*
