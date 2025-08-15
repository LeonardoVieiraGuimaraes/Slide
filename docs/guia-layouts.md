# Guia de Layouts de Slides - Newton Paiva Style

## 📋 Layouts Básicos

### 1. Slide de Título de Seção
```latex
\slidetitulo{Nome da Seção}
```

### 2. Slide Limpo (sem cabeçalho)
```latex
\slidelimpo{
    % Seu conteúdo aqui
}
```

### 3. Slide Centralizado
```latex
\slidecentralizado{Título}{
    % Conteúdo centralizado
}
```

## 🏛️ Layouts com Colunas

### 4. Duas Colunas
```latex
\slideduascolunas{Título}{
    % Conteúdo coluna esquerda
}{
    % Conteúdo coluna direita
}
```

### 5. Três Colunas
```latex
\slidetrescolunas{Título}{
    % Coluna 1
}{
    % Coluna 2
}{
    % Coluna 3
}
```

## 🖼️ Layouts com Imagens

### 6. Imagem Grande e Texto
```latex
\slideimagemtexto{Título}{caminho/para/imagem.png}{
    % Texto explicativo
}
```

### 7. Lista e Imagem
```latex
\slidelistaimagem{Título}{
    % Lista de itens
}{caminho/para/imagem.png}
```

## 🎯 Layouts Especializados

### 8. Comparação (Dois Blocos)
```latex
\slidecomparacao{Título}{Primeiro Item}{
    % Conteúdo primeiro bloco
}{Segundo Item}{
    % Conteúdo segundo bloco
}
```

### 9. Citação
```latex
\slidecitacao{Texto da citação}{Autor}{Fonte/contexto}
```

### 10. Timeline/Processo
```latex
\slidetimeline{Título}{
    % Conteúdo do processo
}
```

### 11. Dados/Gráficos
```latex
\slidedados{Título}{
    % Texto explicativo dos dados
}{
    % Área para gráfico/tabela
}
```

### 12. Contato/Informações
```latex
\slidecontato{
    % Informações de contato
}
```

### 13. Seção Completa
```latex
\secaocompleta{Nome da Seção}
```

### 14. Mídia/Vídeo
```latex
\slidemidia{Título}{Descrição da mídia}{Informações adicionais}
```

### 15. Exemplo/Demonstração
```latex
\slideexemplo{Título}{
    % Conteúdo do exemplo
}
```

### 16. Agradecimentos
```latex
\slideagradecimentos
```

### 17. Sumário/Agenda
```latex
\slidesumario{Título}{
    % Lista da agenda
}
```

### 18. Quiz/Pergunta
```latex
\slidequiz{Título}{Pergunta}{
    % Opções ou instruções
}
```

### 19. Conceito/Definição
```latex
\slideconceito{Título}{Termo}{Definição do termo}
```

### 20. Antes e Depois
```latex
\slideantesdepois{Título}{
    % Situação anterior
}{
    % Situação posterior
}{Observação adicional}
```

## 🎨 Sistema de Alternância de Cabeçalhos

### Durante a apresentação, você pode alternar entre cabeçalhos:

```latex
\usarcabecalhosimples       % Logo pequeno apenas
\usarcabecalhopadrao        % Logo + disciplina + linhas
\usarcabecalhocompleto      % Logo + disciplina + seção
\usarcabecalhoinstitucional % Logo + instituição + professor
\usarcabecalholimpo         % Sem cabeçalho
```

## 🎭 Sistema de Alternância de Estilos

### Mude os estilos durante a apresentação:

```latex
\usarestilopadrao           % Estilo tradicional
\usarestilomoderno          % Cores vibrantes
\usarestilominimalista      % Visual limpo
\usarestiloinstitucional    % Cores Newton Paiva
\usarestiloescuro           % Para fundos escuros
```

## 🌟 Temas Completos para Seções

### Aplicam cabeçalho + estilo automaticamente:

```latex
\temaintroducao         % Cabeçalho simples + estilo padrão
\temadesenvolvimento    % Cabeçalho padrão + estilo moderno
\temaconceitos          % Cabeçalho completo + estilo institucional
\temaexemplos           % Cabeçalho padrão + estilo minimalista
\temaconclusao          % Cabeçalho simples + estilo escuro
\temainstitucional      % Cabeçalho institucional + estilo institucional
```

## 📚 Exemplo de Uso Completo

```latex
\documentclass[aspectratio=169]{beamer}
\usepackage[utf8]{inputenc}
\usepackage[brazilian]{babel}
\usepackage{../styles/newton-paiva-style}

\disciplina{Minha Disciplina}
\instituicao{Centro Universitário Newton Paiva}
\professor{Prof. Meu Nome}

\begin{document}

% Capa
\maketitle

% Agenda
\slidesumario{Agenda}{
    \begin{enumerate}
        \item Introdução
        \item Desenvolvimento
        \item Conclusão
    \end{enumerate}
}

% Mudança de tema
\temaintroducao

% Slide de título de seção
\slidetitulo{Introdução}

% Slide normal
\begin{frame}{Tópico Normal}
    Conteúdo normal do slide
\end{frame}

% Slide com duas colunas
\slideduascolunas{Comparação}{
    Coluna esquerda
}{
    Coluna direita
}

% Mudança de tema
\temadesenvolvimento

% Continue sua apresentação...

% Agradecimentos
\slideagradecimentos

\end{document}
```

## 💡 Dicas de Uso

1. **Planeje os temas**: Use diferentes temas para diferentes seções
2. **Varie os layouts**: Não use sempre o mesmo tipo de slide
3. **Imagens**: Coloque imagens na pasta `assets/images/`
4. **Teste primeiro**: Compile um exemplo antes de criar a apresentação completa
5. **Flexibilidade**: Você pode misturar layouts normais com layouts especiais

## 🔧 Personalização

Todos os layouts podem ser personalizados editando o arquivo `newton-paiva-style.sty`. As cores, fontes e espaçamentos estão definidos no início do arquivo.
