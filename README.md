# Etiqueta Shopee — Level 3D Store

Unificador de etiquetas de postagem Shopee com lista de empacotamento.

## Como funciona

1. Upload do PDF das etiquetas (gerado pela Shopee)
2. Upload do XLSX da lista de empacotamento (exportado da Shopee)
3. Configurar campos, ordenação e mensagem personalizada
4. Processar e imprimir as etiquetas unificadas

## Deploy na Vercel

### Opção 1: Via GitHub (Recomendado)

1. Crie um repositório no GitHub e faça push deste projeto:
   ```bash
   cd etiqueta-shopee
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/SEU-USUARIO/etiqueta-shopee.git
   git push -u origin main
   ```

2. Acesse [vercel.com](https://vercel.com) e faça login
3. Clique em **"Add New Project"**
4. Importe o repositório `etiqueta-shopee`
5. A Vercel vai detectar automaticamente as configurações do `vercel.json`
6. Clique em **"Deploy"**

### Opção 2: Via CLI da Vercel

1. Instale a CLI da Vercel:
   ```bash
   npm install -g vercel
   ```

2. Faça login:
   ```bash
   vercel login
   ```

3. Deploy:
   ```bash
   cd etiqueta-shopee
   vercel --prod
   ```

## Estrutura do Projeto

```
etiqueta-shopee/
├── public/
│   └── index.html    ← Aplicação completa (HTML + CSS + JS)
├── package.json
├── vercel.json       ← Configuração da Vercel
└── README.md
```

## Funcionalidades

- Detecta automaticamente 1, 2 ou 4 etiquetas por página do PDF
- Cruza etiquetas com a lista via código de rastreio (tracking number)
- Campos configuráveis: Quantidade, SKU, Nome do produto, Variação, etc.
- Ordenação drag-and-drop dos campos
- Tamanho de fonte ajustável
- Ordenação por diversos critérios
- Mensagem personalizada no rodapé
- Modo Coleta/Retirada
- Impressão individual ou em lote
