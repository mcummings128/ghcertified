---
question: "Você tem um segredo codificado em base-64 que você decodifica em um workflow de GitHub Actions. Como você pode garantir que o segredo decodificado não apareça acidentalmente no log do workflow?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/workflow-commands#masking-a-value-in-a-log"
---

- [x] Usando o comando `add-mask` no workflow em trabalhos onde o segredo decodificado possa ser utilizado.
> Usar `add-mask` ocultará valores que o GitHub Actions não detecta como segredo. Isso precisa ser feito uma vez por valor, por trabalho que utilize o segredo decodificado.
- [ ] Nada precisa ser feito, já que a infraestrutura do GitHub Actions automaticamente oculta segredos decodificados.
> Não é garantido que o GitHub Actions será capaz de detectar automaticamente e ocultar segredos transformados conforme a [documentação](https://docs.github.com/en/actions/reference/security/secure-use#use-secrets-for-sensitive-information).  
- [ ] Evitar o uso de instruções de impressão que contenham o segredo decodificado, já que esta é a única maneira de o segredo decodificado aparecer no log do workflow.
> Embora evitar instruções de impressão que contenham segredos decodificados seja recomendado, segredos decodificados podem aparecer em outros lugares no log do workflow, como em mensagens relacionadas a chamadas de API.
- [ ] Usar a função integrada `maskSecret` para ocultar o segredo decodificado em instâncias onde ele possa ser utilizado.
> `maskSecret` não é uma função integrada fornecida pelo GitHub Actions.
