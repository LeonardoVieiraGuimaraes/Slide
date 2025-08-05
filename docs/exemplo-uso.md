# Exemplo de Apresentação - Newton Paiva

Este é um exemplo de como criar uma apresentação usando os templates disponíveis.

## Estrutura Recomendada

1. **Slide de Título**: Apresente o tema e autor
2. **Sumário**: Liste os tópicos principais
3. **Introdução**: Contextualize o tema
4. **Desenvolvimento**: Conteúdo principal dividido em seções
5. **Conclusão**: Resumo e considerações finais
6. **Agradecimentos**: Slide final para perguntas

## Elementos Úteis do Beamer

### Blocos
- `block`: Para informações gerais
- `alertblock`: Para informações importantes/alertas
- `exampleblock`: Para exemplos

### Listas
- Use `itemize` para listas com bullets
- Use `enumerate` para listas numeradas
- Use `description` para listas de definições

### Figuras
```latex
\begin{figure}
    \centering
    \includegraphics[width=0.8\textwidth]{assets/images/figura.png}
    \caption{Legenda da figura}
\end{figure}
```

### Colunas
```latex
\begin{columns}
    \begin{column}{0.5\textwidth}
        Conteúdo da primeira coluna
    \end{column}
    \begin{column}{0.5\textwidth}
        Conteúdo da segunda coluna
    \end{column}
\end{columns}
```
