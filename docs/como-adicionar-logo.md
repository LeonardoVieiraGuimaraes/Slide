# Como Adicionar o Logo da Newton Paiva

## 📥 Salvando a Imagem do Logo

1. **Salve a imagem do logo** como:
   - Nome do arquivo: `logNewtonPaiva.png`
   - Local: `assets/logos/logNewtonPaiva.png`

2. **Formatos suportados:**
   - PNG (recomendado)
   - JPG
   - PDF (vetorial)

## 🎨 Templates Disponíveis

### Template Básico (`base-template.tex`)
- Logo no cabeçalho de todos os slides
- Configuração simples

### Template Newton Paiva (`newton-paiva-template.tex`)
- Cores oficiais da Newton Paiva
- Logo integrado na página de título
- Comando `\newtonlogo[tamanho]` para inserir logo

## 🔧 Como Usar o Logo

### No template básico:
```latex
% Logo automaticamente no cabeçalho
\logo{\includegraphics[height=1.2cm]{assets/logos/logNewtonPaiva.png}}
```

### No template Newton Paiva:
```latex
% Logo na página de título (automático)
% ou em qualquer lugar do slide:
\newtonlogo[1.5cm]  % Tamanho personalizável
```

## 🎨 Nova Cor de Fundo

O template agora inclui uma cor de fundo personalizada:
- **Cor:** `#5c2438` (vinho escuro)
- **Texto:** Branco para alto contraste
- **Blocos:** Cores ajustadas para legibilidade

## 🎯 Próximos Passos

1. Salve o logo na pasta correta
2. Escolha um template
3. Copie para `presentations/`
4. Compile com um dos scripts fornecidos
5. Seu slide estará pronto com o logo oficial!

## 📋 Resolução de Problemas

**Se o logo não aparecer:**
- Verifique se o arquivo está em `assets/logos/logNewtonPaiva.png`
- Confirme que o nome do arquivo está correto
- Certifique-se de que a extensão é `.png`
