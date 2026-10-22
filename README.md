# Nossa rotina semanal

Quadro interativo para Mateus, Débora e Nikova, hospedado em GitHub Pages com registros compartilhados em Supabase.

- Escolha de perfil antes de entrar; a escolha identifica o autor e não verifica identidade por senha.
- Confirmação antes de concluir ou desmarcar, com nome e horário registrados no servidor.
- 35 tarefas semanais, progresso e revezamento automático desde 19/10/2026.
- Dia atual destacado no fuso America/Sao_Paulo, com atalho para suas tarefas.
- Atualizações compartilhadas a cada 10 segundos enquanto a página está visível.
- Erros de gravação são exibidos; a conclusão só aparece salva após resposta do banco.
- Layout responsivo, teclado e rótulos acessíveis.

## Acesso da casa

Use o link privado fornecido ao casal. O fragmento #casa=CHAVE permite acesso aos registros e não está no repositório. O botão de compartilhar copia esse link; compartilhe somente entre vocês. A chave fica salva no navegador para acessos seguintes. A página sempre pede o perfil ao abrir. Limpar o navegador não apaga os registros do servidor; basta abrir novamente o link privado.

`sync-config.js` contém apenas a URL e chave publishable públicas do Supabase. Nunca inserir service_role ou a chave privada da casa no código público. As tabelas usam RLS sem acesso direto e as funções validam a chave privada por SHA-256. O SQL de referência está em backend/schema.sql nos arquivos entregues. O histórico local da versão anterior não é importado automaticamente.

## GitHub Pages

Settings → Pages → Deploy from a branch → main → / (root). Arquivos necessários na raiz: index.html, style.css, app.js, sync-config.js.

## Validação

Fluxos verificados no navegador: seleção de ambos os perfis, cancelamento sem concluir, confirmação de conclusão, leitura pelo outro perfil após recarregar, desmarcação confirmada e destaque do dia atual. Banco provisionado na região São Paulo.
