# Degelo MB - Release 0.0.12

Data: 2025-11-10

Este release atualiza o aplicativo desktop para a versão 0.0.12 e prepara o repositório de updates para o auto-update.

Principais mudanças:
- Busca de operadores controlada e com normalização de acentos na página Operadores
- Botão de exclusão com diálogo de confirmação e feedback via toast
- Hook `useDeleteOperator` integrado ao Supabase
- Migrações RLS adicionadas e aplicadas:
  - `DELETE` em `public.operadores` somente quando não referenciados por `defrost_cycles`
  - `INSERT` e `UPDATE` protegidos e com colunas restritas
- README do projeto principal atualizado com políticas de segurança e RLS

Observações de segurança:
- RLS ativa para todas as operações em `public.operadores`
- Exclusões bloqueadas quando houver referência em `defrost_cycles`

Próximos passos:
- Publicação dos assets do release (installer .exe e latest.yml) via GitHub Actions (electron-builder)
- Verificar se o release foi publicado nas Releases do repositório `degelo-mb-updates` com a tag `v0.0.12`
