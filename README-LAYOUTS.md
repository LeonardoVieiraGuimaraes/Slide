# 🎨 Sistema de Múltiplos Layouts - Newton Paiva Style

## ✨ Visão Geral
O `newton-paiva-style.sty` agora oferece um sistema completo de layouts múltiplos, similar ao PowerPoint, permitindo criar apresentações variadas e dinâmicas.

## 📋 Layouts Disponíveis

### 🏛️ **Layouts Básicos**

#### 1. Slide de Título de Seção
```latex
\slidetitulo{Nome da Seção}
```
- Cria um slide para marcar o início de uma nova seção
- Logo centralizado + título grande + linha decorativa

#### 2. Slide Limpo (sem cabeçalho)
```latex
\slidelimpo{
    % Seu conteúdo aqui
}
```
- Remove completamente o cabeçalho
- Ideal para slides especiais, citações, etc.

#### 3. Slide Centralizado
```latex
\slidecentralizado{Título}{
    % Conteúdo centralizado
}
```
- Centraliza o conteúdo vertical e horizontalmente
- Ótimo para conceitos importantes

### 🖼️ **Layouts com Colunas**

#### 4. Duas Colunas
```latex
\slideduascolunas{Título}{
    % Conteúdo coluna esquerda
}{
    % Conteúdo coluna direita
}
```

#### 5. Três Colunas
```latex
\slidetrescolunas{Título}{
    % Coluna 1
}{
    % Coluna 2
}{
    % Coluna 3
}
```

### 🎯 **Layouts Especializados**

#### 6. Citação
```latex
\slidecitacao{Texto da citação}{Autor}{Fonte/contexto}
```
- Destaca citações importantes em caixa especial

#### 7. Conceito/Definição
```latex
\slideconceito{Título}{Termo}{Definição do termo}
```
- Apresenta definições de forma destacada

#### 8. Agenda/Sumário
```latex
\slidesumario{Título}{
    \begin{enumerate}
        \item Item 1
        \item Item 2
    \end{enumerate}
}
```

#### 9. Seção Completa
```latex
\secaocompleta{Nome da Seção}
```
- Slide especial para separar seções principais

#### 10. Agradecimentos
```latex
\slideagradecimentos
```
- Slide automático de encerramento

## 🎨 **Sistema de Alternância**

### Mudando Cabeçalhos Durante a Apresentação
```latex
\usarcabecalhosimples       % Logo pequeno apenas
\usarcabecalhopadrao        % Logo + disciplina + linhas
\usarcabecalhocompleto      % Logo + disciplina + seção
\usarcabecalhoinstitucional % Logo + instituição + professor
\usarcabecalholimpo         % Sem cabeçalho
```

### Mudando Estilos Durante a Apresentação
```latex
\usarestilopadrao           % Estilo tradicional
\usarestilomoderno          % Cores vibrantes
\usarestilominimalista      % Visual limpo
\usarestiloinstitucional    % Cores Newton Paiva
\usarestiloescuro           % Para fundos escuros
```

### Temas Completos para Seções
```latex
\temaintroducao         % Cabeçalho simples + estilo padrão
\temadesenvolvimento    % Cabeçalho padrão + estilo moderno
\temaconceitos          % Cabeçalho completo + estilo institucional
\temaexemplos           % Cabeçalho padrão + estilo minimalista
\temaconclusao          % Cabeçalho simples + estilo escuro
\temainstitucional      % Cabeçalho institucional + estilo institucional
```

## 🚀 **Exemplo de Uso Prático**

```latex
\documentclass[aspectratio=169]{beamer}
\usepackage[utf8]{inputenc}
\usepackage[brazilian]{babel}
\usepackage{styles/newton-paiva-style}

\disciplina{Minha Disciplina}
\instituicao{Centro Universitário Newton Paiva}
\professor{Prof. Meu Nome}

\begin{document}

% === CAPA ===
\maketitle

% === AGENDA ===
\slidesumario{Agenda}{
    \begin{enumerate}
        \item Introdução
        \item Desenvolvimento  
        \item Exemplos
        \item Conclusão
    \end{enumerate}
}

% === SEÇÃO 1: INTRODUÇÃO ===
\temaintroducao  % Aplica tema completo
\slidetitulo{Introdução}

\begin{frame}{Conceitos Básicos}
    Conteúdo normal do slide...
\end{frame}

\slideconceito{Definição}{Termo Importante}{Explicação do termo...}

% === SEÇÃO 2: DESENVOLVIMENTO ===
\temadesenvolvimento  % Muda para tema moderno
\slidetitulo{Desenvolvimento}

\slideduascolunas{Comparação}{
    \begin{itemize}
        \item Método A
        \item Vantagem 1
        \item Vantagem 2
    \end{itemize}
}{
    \begin{itemize}
        \item Método B
        \item Vantagem X
        \item Vantagem Y
    \end{itemize}
}

% === SEÇÃO 3: EXEMPLOS ===
\temaexemplos
\slidetitulo{Exemplos Práticos}

\slidecentralizado{Exemplo Principal}{
    \Large Conteúdo destacado e centralizado
}

% === CONCLUSÃO ===
\temaconclusao
\slidetitulo{Conclusão}

\slidecitacao{O conhecimento é poder}{Francis Bacon}{Meditationes Sacrae, 1597}

% === ENCERRAMENTO ===
\slideagradecimentos

\end{document}
```

## 💡 **Dicas de Uso**

1. **Planeje os temas**: Use diferentes temas para diferentes seções da apresentação
2. **Varie os layouts**: Não use sempre o mesmo tipo de slide
3. **Teste primeiro**: Compile exemplos antes de criar a apresentação completa
4. **Flexibilidade**: Você pode misturar layouts especiais com slides normais

## 🔧 **Personalização**

- Todas as cores estão definidas no início do arquivo `newton-paiva-style.sty`
- Os layouts podem ser personalizados editando os comandos correspondentes
- Novos layouts podem ser adicionados seguindo o padrão existente

## 📁 **Arquivos de Exemplo**

- `exemplo-layouts-simples.tex` - Demonstra os principais layouts
- `guia-layouts.md` - Referência completa de comandos
- `newton-paiva-template.tex` - Template básico para começar

---

**🎓 Centro Universitário Newton Paiva**  
*Sistema de templates para apresentações acadêmicas*
