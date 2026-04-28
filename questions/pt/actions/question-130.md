---
question: "Quais das seguintes afirmações são verdadeiras sobre blocos de `outputs` em nível de fluxo de trabalho versus em nível de trabalho?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/workflow-syntax#example-defining-outputs-for-a-job"
---

- [ ] Blocos de `outputs` em nível de trabalho devem ser usados apenas em fluxos de trabalho chamadores, não em fluxos de trabalho reutilizáveis.
> Fluxos de trabalho reutilizáveis podem ter blocos de `outputs` tanto em nível de trabalho quanto em nível de fluxo de trabalho.
- [x] Um bloco de `outputs` em nível de fluxo de trabalho deve ser usado apenas em fluxos de trabalho reutilizáveis, não em fluxos de trabalho chamadores.
> Um bloco de `outputs` em nível de "fluxo de trabalho" refere-se a um bloco de `outputs` que é filho direto de `workflow_call` em fluxos de trabalho reutilizáveis. Em fluxos de trabalho não reutilizáveis, blocos de `outputs` devem estar presentes apenas em nível de trabalho.
- [x] Um fluxo de trabalho reutilizável pode ter blocos de `outputs` tanto em nível de fluxo de trabalho quanto em nível de trabalho.
> Se for desejado definir uma saída em um fluxo de trabalho reutilizável e passar essa mesma saída para um fluxo de trabalho chamador, devem ser usados blocos de `outputs` em nível de fluxo de trabalho e em nível de trabalho. 
> Veja a documentação para mais detalhes https://docs.github.com/en/actions/how-tos/reuse-automations/reuse-workflows#using-outputs-from-a-reusable-workflow
- [ ] Um bloco de `outputs` em nível de trabalho deve ter a seguinte estrutura:
```
outputs:
    <output-name>
        value: ${{ steps.<step-name>.outputs.<output-name> }}
```
> Um bloco de `outputs` em nível de trabalho utiliza uma estrutura não aninhada de pares `key=value`. Veja a documentação oficial (https://docs.github.com/en/actions/reference/workflows-and-actions/workflow-syntax#example-defining-outputs-for-a-job) para mais detalhes.
- [x] Um bloco de `outputs` em nível de fluxo de trabalho deve ter a seguinte estrutura:
```
outputs:
    <output-name>
        value: ${{ jobs.<job-name>.outputs.<output-name> }}
```
> Um bloco de `outputs` em nível de fluxo de trabalho deve seguir a estrutura acima. A chave `value` é sempre obrigatória. Uma chave opcional `description` também pode ser usada (não mostrada no exemplo acima). 
> Veja a documentação para mais detalhes - https://docs.github.com/en/actions/how-tos/reuse-automations/reuse-workflows#using-outputs-from-a-reusable-workflow
