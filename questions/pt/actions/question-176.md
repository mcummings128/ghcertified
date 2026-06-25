---
question: "Judith tem um fluxo de trabalho que deve ser acionado sempre que um commit for feito no repositório. O repositório nem sempre é tão ativo, então Judith deseja que o fluxo de trabalho seja executado programaticamente uma vez por semana como uma medida de segurança. Que combinação de eventos ela deve usar para garantir esse comportamento?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows"
---

- [x] `push` e `schedule`
- [ ] `pull_request` (com `types:[closed]`) e `schedule`
> Pull requests podem ser fechados sem serem mesclados, e commits podem ser feitos em um repositório sem um pull request.
- [ ] `push` e `workflow_dispatch`
> A palavra "programaticamente" na pergunta significa que o fluxo de trabalho deve ser acionado de forma não manual. Fazer com que os usuários ativem manualmente um fluxo de trabalho toda semana não é confiável — isso pode e deve ser automatizado com `schedule`.
- [ ] `push` e `weekly`
> `weekly` não é um evento válido. Utilize `schedule` com sintaxe `cron` para configurar o fluxo de trabalho para ser executado semanalmente.
- [ ] Isso não é possível: `schedule` não pode ser combinado com outros eventos
