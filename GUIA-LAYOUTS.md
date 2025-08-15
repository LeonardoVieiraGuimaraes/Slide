# 🎨 Sistema de Layouts Newton Paiva

## 📋 Guia Rápido de Uso

### 🚀 Início Rápido

1. **Use o novo pacote de estilos:**
   ```latex
   \usepackage{../styles/newton-paiva-layouts}
   ```

2. **Configure suas informações:**
   ```latex
   \disciplina{Sua Disciplina}
   \professor{Seu Nome}
   \secaoatual{Sua Seção}
   ```

3. **Escolha um title page e layouts para slides**

---

## 🎭 Title Pages Disponíveis

### `\titlepagepadrao`
- **Layout:** 2 colunas (texto + imagem)
- **Uso:** Apresentações gerais
- **Características:** Disciplina + instituição + professor + data

### `\titlepagemoderno`
- **Layout:** Horizontal com título em destaque
- **Uso:** Apresentações impactantes
- **Características:** Título grande + elementos visuais

### `\titlepageclassico`
- **Layout:** Centralizado vertical
- **Uso:** Apresentações formais
- **Características:** Logo + informações centralizadas

---

## 🎯 Layouts de Slides

### `\layoutpadrao`
- **Cabeçalho:** Logo + disciplina + linhas
- **Rodapé:** Numeração simples
- **Uso:** Slides de conteúdo normal

### `\layoutapresentacao`
- **Cabeçalho:** Logo + disciplina + seção + professor
- **Rodapé:** Disciplina + professor + numeração
- **Uso:** Apresentações formais, defesas

### `\layoutaula`
- **Cabeçalho:** Logo + disciplina + linhas
- **Rodapé:** Disciplina + professor + numeração
- **Uso:** Aulas, explicações didáticas

### `\layoutexercicio`
- **Cabeçalho:** Apenas logo pequeno
- **Rodapé:** Numeração simples
- **Uso:** Exercícios, atividades práticas

### `\layoutsecao`
- **Cabeçalho:** Logo + instituição + professor
- **Rodapé:** Sem rodapé
- **Uso:** Slides de seção, transições

### `\layoutlimpo`
- **Cabeçalho:** Sem cabeçalho
- **Rodapé:** Sem rodapé
- **Uso:** Slides de impacto, conclusões

---

## 🎨 Personalização Avançada

### Cabeçalhos Individuais
```latex
\cabecalhopadrao          % Logo + disciplina + linhas
\cabecalhosimples         % Apenas logo pequeno
\cabecalhocompleto        % Logo + disciplina + seção + professor
\cabecalhoinstitucional   % Logo + instituição + professor
\cabecalhominimalista     % Apenas linha decorativa
\cabecalholimpo           % Sem cabeçalho
```

### Rodapés Individuais
```latex
\rodapepadrao             % Numeração simples
\rodapecompleto          % Disciplina + professor + numeração
\rodapelimpo             % Sem rodapé
```

---

## 📝 Exemplo de Uso

```latex
\documentclass[aspectratio=169]{beamer}
\usepackage{../styles/newton-paiva-layouts}

% Configurações
\disciplina{Minha Disciplina}
\professor{Meu Nome}
\secaoatual{Introdução}

\begin{document}

% Title page
\titlepagepadrao
\begin{frame}[plain]
    \maketitle
\end{frame}

% Slides normais
\layoutpadrao
\begin{frame}{Meu Slide}
    Conteúdo aqui...
\end{frame}

% Slide de seção
\layoutsecao
\begin{frame}
    \begin{center}
        \Huge{Nova Seção}
    \end{center>
\end{frame>

% Slide de exercício
\layoutexercicio
\begin{frame}{Exercício}
    Pergunta aqui...
\end{frame>

\end{document>
```

---

## 🎨 Cores Disponíveis

- `newtonpurple` - Roxo oficial Newton Paiva
- `newtanorange` - Laranja oficial Newton Paiva
- `newtonbackground` - Cor de fundo (#5c2438)
- `newtonblue` - Azul Newton Paiva
- `newtonlightblue` - Azul claro
- `newtongray` - Cinza padrão

---

## 📁 Estrutura de Arquivos

```
projeto/
├── styles/
│   ├── newton-paiva-layouts.sty    (novo sistema)
│   └── newton-paiva-style.sty      (sistema antigo)
├── templates/
│   ├── exemplo-layouts-multiplos.tex
│   └── template-simples-layouts.tex
└── assets/
    └── logos/
        └── logNewtonPaiva.png
```

---

## 🔧 Dicas de Uso

1. **Mude layouts conforme necessário** - Use diferentes layouts para diferentes tipos de slides
2. **Seja consistente** - Mantenha um padrão dentro de cada seção
3. **Use cores Newton Paiva** - `newtanorange` para destaques, `newtonpurple` para títulos
4. **Teste diferentes title pages** - Escolha o que melhor se adequa ao seu público
5. **Combine cabeçalhos e rodapés** - Personalize além dos layouts pré-definidos

---

## 🆘 Solução de Problemas

**Logo não aparece:**
- Verifique se `logNewtonPaiva.png` está em `assets/logos/`
- O sistema tem fallback automático

**Layout não muda:**
- Certifique-se de colocar o comando antes do `\begin{frame}`
- Use `\layoutpadrao` para voltar ao padrão

**Cores estranhas:**
- Verifique se está usando as cores Newton Paiva
- Use `\textcolor{white}` para texto em fundo escuro
