---
question: "Hilda precisa acessar um artefato gerado por uma execução de fluxo de trabalho recente, mas o arquivo de fluxo de trabalho em si foi excluído. Ela ainda conseguirá recuperar o artefato?"
documentation: "https://docs.github.com/en/actions/how-tos/manage-workflow-runs/remove-workflow-artifacts#artifacts-from-deleted-workflow-runs"
---

- [x] Sim, porque excluir um fluxo de trabalho não apaga automaticamente suas execuções e artefatos gerados
> As execuções de fluxo de trabalho e os artefatos gerados não são automaticamente apagados quando o fluxo de trabalho correspondente é excluído. É necessário apagar a própria execução para excluir os artefatos.
- [ ] Não, porque excluir um fluxo de trabalho automaticamente apaga suas execuções e artefatos gerados
- [ ] Sim, mas apenas se ela tiver privilégios de administrador
- [ ] Não, porque, embora as execuções de fluxo de trabalho permaneçam após a exclusão de um fluxo de trabalho, os artefatos gerados ficam corrompidos
