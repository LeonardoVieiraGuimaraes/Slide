# Guia de Gradientes Newton Paiva

## Visão Geral

O sistema de gradientes Newton Paiva oferece 4 opções de plano de fundo baseadas nas cores da identidade visual da instituição, extraídas diretamente da imagem fornecida.

## Cores Utilizadas

- **Roxo/Magenta**: `RGB(142, 45, 153)` - Cor principal do gradiente
- **Cor Intermediária**: `RGB(165, 55, 120)` - Tom médio para transições
- **Laranja/Vermelho**: `RGB(235, 94, 40)` - Cor de destaque

## Comandos Disponíveis

### 1. Gradiente Horizontal (Padrão)
```latex
\fundogradiente
```
- **Descrição**: Gradiente da esquerda (roxo) para direita (laranja)
- **Uso**: Slides normais de conteúdo
- **Características**: Ativado automaticamente, melhor legibilidade

### 2. Gradiente Vertical
```latex
\fundogradientevertical
```
- **Descrição**: Gradiente de cima (roxo) para baixo (laranja)
- **Uso**: Slides de seção, apresentações dramáticas
- **Características**: Efeito visual forte, destaque vertical

### 3. Gradiente Radial
```latex
\fundogradienteradial
```
- **Descrição**: Gradiente do centro (intermediário) para bordas (roxo)
- **Uso**: Slides de foco central, conclusões importantes
- **Características**: Destaca o conteúdo central, efeito de profundidade

### 4. Fundo Sólido Original
```latex
\fundosolido
```
- **Descrição**: Retorna ao fundo sólido tradicional Newton Paiva
- **Uso**: Compatibilidade, impressão, ambientes conservadores
- **Características**: Cor sólida `#5c2438`

## Como Usar

### Configuração Inicial
1. Certifique-se de usar o pacote: `\usepackage{../styles/newton-paiva-layouts}`
2. O gradiente horizontal é ativado automaticamente

### Mudando o Plano de Fundo
Coloque o comando do gradiente desejado **antes** do slide que você quer alterar:

```latex
% Exemplo: mudando para gradiente vertical
\fundogradientevertical

\begin{frame}{Título do Slide}
    % Conteúdo do slide com fundo vertical
\end{frame}

% Voltando para gradiente horizontal
\fundogradiente

\begin{frame}{Próximo Slide}
    % Conteúdo com fundo horizontal
\end{frame}
```

## Exemplos de Uso

### Apresentação Típica
```latex
% Título com gradiente padrão
\titlepagepadrao
\begin{frame}[plain]
    \maketitle
\end{frame}

% Slides normais (gradiente horizontal já ativo)
\begin{frame}{Conteúdo Normal}
    % Seu conteúdo aqui
\end{frame}

% Slide de nova seção
\fundogradientevertical
\begin{frame}{Nova Seção}
    % Slide de transição
\end{frame}

% Voltando ao normal
\fundogradiente
\begin{frame}{Continuação}
    % Mais conteúdo
\end{frame}

% Slide de conclusão com destaque central
\fundogradienteradial
\begin{frame}{Conclusões}
    % Pontos finais
\end{frame}
```

## Dicas de Design

### Gradiente Horizontal
- ✅ **Use para**: Slides de conteúdo normal
- ✅ **Vantagens**: Melhor legibilidade, não interfere com texto
- ✅ **Combina com**: Todos os layouts de cabeçalho

### Gradiente Vertical
- ✅ **Use para**: Slides de transição, títulos de seção
- ⚠️ **Cuidado**: Pode interferir com texto se mal posicionado
- ✅ **Combina com**: Layouts limpos, texto centralizado

### Gradiente Radial
- ✅ **Use para**: Destaque de conteúdo central, conclusões
- ✅ **Vantagens**: Cria foco visual no centro
- ⚠️ **Cuidado**: Use com moderação, pode cansar visualmente

### Fundo Sólido
- ✅ **Use para**: Máxima compatibilidade
- ✅ **Vantagens**: Funciona em qualquer situação
- ✅ **Ideal para**: Impressão, projetores antigos

## Requisitos Técnicos

- **Pacote necessário**: `tikz` (incluído automaticamente)
- **Compilador**: XeLaTeX ou LuaLaTeX (recomendado)
- **Formato**: Aspect ratio 16:9 configurado automaticamente

## Compatibilidade

- ✅ Todos os layouts de cabeçalho
- ✅ Todos os layouts de rodapé  
- ✅ Title pages padrão, moderno e clássico
- ✅ Blocos e elementos do beamer
- ✅ Cores de texto otimizadas

## Troubleshooting

### Gradiente não aparece
- Verifique se o pacote `tikz` está instalado
- Use XeLaTeX ou LuaLaTeX como compilador

### Texto ilegível
- Use cores de texto adequadas (branco, amarelo claro)
- Considere usar o fundo sólido para melhor contraste

### Performance lenta
- Gradientes podem tornar a compilação mais lenta
- Use o fundo sólido durante desenvolvimento rápido
