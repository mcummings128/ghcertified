---
question: "Marianne tem um branch de funcionalidade que contém seu novo arquivo de workflow, configurado para ser acionado às 2h da manhã todos os dias, usando a sintaxe abaixo. No entanto, no dia seguinte, o workflow não é acionado. Por que isso pode ter acontecido?"
documentation: "https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows#schedule"
---

```yaml
on:
    schedule:
        cron:
            "0 2 * * *"
```

- [x] O arquivo de workflow deve estar no branch padrão para ser acionado pelo evento `schedule`
- [ ] A sintaxe `cron` não está configurada corretamente
> `"0 2 * * *"` na sintaxe CRON significa "executar todos os dias às 2h da manhã." Mesmo que a programação estivesse configurada incorretamente, o workflow ainda não seria acionado, pois ele não está presente no branch padrão.
- [ ] `schedule` não pode ser o único evento no workflow. Ele deve ser combinado com um evento baseado em repositório, como `push`
- [ ] A sintaxe `@daily` não foi utilizada
> Sintaxes CRON não padronizadas, como `@daily`, não são suportadas pelo GitHub Actions.
- [ ] O repositório privado que contém o workflow não teve nenhuma atividade há mais de 60 dias, desativando automaticamente o workflow.
> Essa desativação automática só ocorre em repositórios públicos, não em repositórios privados.
