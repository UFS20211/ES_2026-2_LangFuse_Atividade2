# Atividade 2 - Auditoria Forense e Plano de Resgate Tecnico

Projeto analisado: **langfuse/langfuse**

## Conteudo
- `relatorio.tex` (Relatorio tecnico)
- `slides.tex` (Apresentacao de impacto)

## Como gerar os PDFs
Use um compilador LaTeX instalado na sua maquina:

```bash
pdflatex relatorio.tex
pdflatex slides.tex
```

Alternativa com Tectonic:

```bash
tectonic relatorio.tex
tectonic slides.tex
```

## Pontos Importantes
- Issue com discussao e mudanca de escopo: https://github.com/langfuse/langfuse/issues/13933
- TODOs em filas criticas:
  - https://github.com/langfuse/langfuse/blob/main/worker/src/queues/otelIngestionQueue.ts#L215-L219
  - https://github.com/langfuse/langfuse/blob/main/worker/src/queues/webhooks.ts#L49-L52
  - https://github.com/langfuse/langfuse/blob/main/worker/src/queues/webhooks.ts#L568-L570
  - https://github.com/langfuse/langfuse/blob/main/packages/shared/src/server/llm/compileChatMessages.ts#L98-L105
- Cadencia de commits: https://github.com/langfuse/langfuse/graphs/contributors e https://github.com/langfuse/langfuse/pulse
- Code review: https://github.com/langfuse/langfuse/pull/13955#issuecomment-4585104387
- Acoplamento de adapters:
  - https://github.com/langfuse/langfuse/blob/main/packages/shared/src/server/llm/types.ts#L252-L259
  - https://github.com/langfuse/langfuse/blob/main/packages/shared/src/server/llm/fetchLLMCompletion.ts#L303-L413
  - https://github.com/langfuse/langfuse/blob/main/web/src/features/llm-api-key/server/router.ts#L100-L140
  - https://github.com/langfuse/langfuse/blob/main/web/src/features/playground/page/hooks/useModelParams.ts#L220-L269
- DRY duplicado: https://github.com/langfuse/langfuse/blob/main/web/src/components/trace2/lib/tree-building.ts#L466
- Singletons:
  - https://github.com/langfuse/langfuse/blob/main/packages/shared/src/db.ts#L8-L18
  - https://github.com/langfuse/langfuse/blob/main/packages/shared/src/server/services/SlackService.ts#L246-L253
- Adapter pattern: https://github.com/langfuse/langfuse/blob/main/packages/shared/src/utils/chatml/adapters/index.ts#L11-L37

## Link do video
Adicionar o link do video aqui: [LINK_DO_VIDEO_AQUI]
