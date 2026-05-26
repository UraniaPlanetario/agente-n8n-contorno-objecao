# RESTORE POINT — Histórico

## ✅ v0.17 (ATIVA — 2026-05-26)

Uso ativo do campo `Objeções (livre)` como contexto prioritário do roteiro. Patch acolhe elementos específicos da citação literal do cliente em todas as falas relevantes (validar, investigar, ancorar). Validado em lead 28231916 (SME) com não-regressão confirmada em 4 leads com #6 isolado.

### Histórico v0.15 → v0.16 → v0.17

- **v0.15** — 3 patches pós-round test (diluição forçada #1+combo, 3 perguntas forçadas #14+combo, datas-âncora trimestrais #9).
- **v0.16** — anti-cópia reforçada para #6 (frases queimadas + variantes). Cópia deslocada, não eliminada — aceita como cosmética.
- **v0.17** — uso ativo de `Objeções (livre)`. Resolve caso SME (lead 28231916).

Detalhes da versão e validação: ver `SYSTEM_PROMPT.md` (histórico de iterações).

## Histórico de mudanças com rollback documentado

- **2026-05-23** — migração field `1378355` → `1378497` (texto curto → texto longo). ✅ Concluída.
- **2026-05-25** — v0.7 → v0.8 (concisão + cabeçalho objeções). ✅ Concluída.
- **2026-05-26** — v0.8 → v0.12 (calibração de tom humano em 4 iterações: v0.9, v0.10, v0.11, v0.12). ✅ Concluída.
- **2026-05-26** — v0.12 → v0.13 → v0.13.1 (cabeçalho clean "Contorno: <label literal>" — sem disclaimer, label Kommo preservado). ✅ Concluída.
- **2026-05-26** — v0.13.1 → v0.14 (regra de multi-objeção: roteiro cobre todas as objeções marcadas). ✅ Concluída.
- **2026-05-26** — v0.14 → v0.15 (round test 54 disparos · 3 patches: diluição forçada #1+combo, 3 perguntas forçadas #14+combo, datas-âncora trimestrais #9). ✅ Concluída.
- **2026-05-26** — v0.15 → v0.16 (anti-cópia reforçada #6, validação em 4 leads reais com cópia 100% — fala 3 melhorou parcial, fala 2 cópia deslocada). ✅ Concluída.
- **2026-05-26** — v0.16 → v0.17 (uso ativo de `Objeções (livre)` — bug descoberto em lead 28231916 SME, validado no mesmo lead pós-patch). ✅ Concluída.

## Como reverter qualquer versão via Git

```bash
git log --oneline --all
git show <hash-do-commit>:SYSTEM_PROMPT.md
git show <hash-do-commit>:.workflow-build.js
```

Aplicar via MCP `n8n_update_partial_workflow` com o conteúdo extraído do commit antigo.

## Próximos pontos de retorno

Documentar aqui antes de mudanças arquiteturais futuras (novos nodes, mudança de modelo LLM, mudança de estrutura de output).
