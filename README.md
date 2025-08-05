# Projeto de Slides - Newton Paiva

Este projeto contém templates e recursos para criação de apresentações em LaTeX usando Beamer.

## 📁 Estrutura do Projeto

```
Slide/
├── templates/          # Templates base para apresentações
│   ├── base-template.tex          # Template básico
│   └── newton-paiva-template.tex  # Template com cores oficiais
├── styles/            # Estilos customizados
│   └── newton-paiva-style.sty
├── assets/            # Recursos visuais
│   ├── images/        # Imagens gerais
│   └── logos/         # Logo Newton Paiva (newton-paiva-logo.png)
├── presentations/     # Suas apresentações finais
├── output/           # PDFs gerados
└── docs/             # Documentação adicional
    └── como-adicionar-logo.md
```

## Como Usar

### 1. Adicionando o Logo Newton Paiva

1. **Salve o logo** como `newton-paiva-logo.png` na pasta `assets/logos/`
2. **Escolha um template:**
   - `base-template.tex`: Template básico com logo no cabeçalho
   - `newton-paiva-template.tex`: Template com cores oficiais da Newton Paiva

### 2. Escolha um template:**
   - `base-template.tex`: Template básico com logo no cabeçalho
   - `newton-paiva-template.tex`: Template com cores oficiais da Newton Paiva

**Características dos templates:**
   - ✅ Formato 16:9 (widescreen)
   - ✅ Logo Newton Paiva no topo de todos os slides
   - ✅ Fundo personalizado cor `#5c2438`
   - ✅ Cores oficiais da instituição
   - ✅ Layout otimizado para apresentações modernas

1. Copie o template escolhido para a pasta `presentations/`
2. Renomeie para o nome da sua apresentação (ex: `minha-apresentacao.tex`)
3. Edite o conteúdo conforme necessário
4. Compile com LaTeX para gerar o PDF

### 4. Usando o Estilo Personalizado

Para usar o estilo Newton Paiva, adicione no preâmbulo do seu documento:

```latex
\documentclass[aspectratio=169]{beamer}  % Formato 16:9
\usepackage{styles/newton-paiva-style}
```

### 5. Compilação

Existem várias formas de compilar seus slides:

#### Opção A: Script PowerShell (Recomendado para Windows)
```powershell
.\compile.ps1 nome-da-apresentacao
```

#### Opção B: Makefile
```bash
make PRESENTATION=nome-da-apresentacao
```

#### Opção C: VS Code Tasks
1. Abra o arquivo `.tex` no VS Code
2. Pressione `Ctrl+Shift+P`
3. Digite "Tasks: Run Task"
4. Selecione "Compilar Apresentação LaTeX"

#### Opção D: Compilação Manual
```bash
# Criar pasta temporária
mkdir temp

# Compilar
pdflatex -output-directory=temp presentations/sua-apresentacao.tex

# Mover PDF para output
move temp/sua-apresentacao.pdf output/
```

**Resultado:** O PDF será gerado na pasta `output/` e os arquivos temporários ficarão em `temp/`.

## Temas Disponíveis

O Beamer oferece vários temas. Alguns populares:
- Madrid (padrão no template)
- Berlin
- CambridgeUS
- Warsaw
- Singapore

Para trocar o tema, altere a linha:
```latex
\usetheme{Madrid}
```

## Recursos Úteis

- **Blocos**: Use `\begin{block}`, `\begin{alertblock}`, `\begin{exampleblock}`
- **Colunas**: Use `\begin{columns}` para layout em colunas
- **Figuras**: Coloque imagens em `assets/images/`
- **Logos**: Coloque logos em `assets/logos/`

## Dicas

1. Mantenha slides simples e limpos
2. Use bullet points ao invés de muito texto
3. Inclua imagens para ilustrar conceitos
4. Teste a apresentação antes de apresentar
5. Salve os PDFs na pasta `output/`
