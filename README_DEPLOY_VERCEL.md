Resumo rápido para deploy no Vercel

Opções recomendadas:

1) Deploy a partir do diretório `catbiosearch-financeiro` (recomendado)
   - No painel do Vercel, ao criar um novo projeto, selecione o repositório e, em "Root Directory" (ou "Project Settings > General > Root Directory"), informe: `catbiosearch-financeiro`
   - Isso garante que o site será servido a partir desse subdiretório e tudo funcionará sem roteamentos extras.

2) Deploy a partir do root do repositório (alternativa)
   - Existe um arquivo `vercel.json` no root que rewriteia as requisições para `catbiosearch-financeiro`.
   - Se preferir não mexer no Root Directory, o `vercel.json` já cuida do redirecionamento para `catbiosearch-financeiro`.

Deploy via Vercel CLI

1. Instale a CLI (se ainda não):

```powershell
npm i -g vercel
```

2. Fazer deploy (opção: deployar apenas o folder)

```powershell
# deploy deployando o subdiretório (recomendado)
cd 'c:\Users\maria\Desktop\Nova pasta\gpa-open-source\catbiosearch-financeiro'
vercel --prod

# OU, deployar a partir do root (vercel.json fará o routing)
cd 'c:\Users\maria\Desktop\Nova pasta\gpa-open-source'
vercel --prod
```

Notas úteis
- Os PDFs estão em `catbiosearch-financeiro/public/balanco-patrimonial/`. Quando o site for servido a partir de `catbiosearch-financeiro` (recomendado), os caminhos usados (`./public/balanco-patrimonial/...`) funcionarão corretamente.
- Se você usar deploy pelo root sem setar Root Directory, o arquivo `vercel.json` mapeia as rotas para `catbiosearch-financeiro`.
- Se encontrar problemas com arquivos acentuados no nome (ex: `BALANÇO`), recomendo renomear para `BALANCO` (sem acento) para evitar problemas em alguns servidores/URLs. Atualmente o site usa nomes com acentos; Vercel geralmente lida bem, mas é mais seguro evitar.

Se quiser eu posso:
- Renomear os PDFs para remover acentos e atualizar os links automaticamente.
- Criar um workflow simples (GitHub Actions) que roda checks antes de deploy.
- Fazer o deploy inicial pra você (preciso que você conecte o repositório ao Vercel ou me dê permissão).