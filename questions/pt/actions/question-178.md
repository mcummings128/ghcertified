---
question: "Você precisa garantir que seu ambiente `prod` exija aprovações manuais antes que os deploys possam prosseguir. Entre as opções a seguir, quais são verdadeiras sobre como isso é configurado?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/deployments-and-environments#required-reviewers"
---

- [x] Se você listar os revisores obrigatórios, apenas um deles precisa aprovar para continuar com o deployment.
- [x] Você pode impedir autoavaliações no caso de a pessoa que deseja fazer o deploy também ser um revisor obrigatório.
- [ ] Se você listar os revisores obrigatórios, todos eles precisam aprovar para continuar com o deployment.
> Surpreendentemente, apenas 1 dos revisores obrigatórios precisa aprovar o job do workflow. Para impor esse comportamento, você precisará criar uma regra personalizada de proteção de deployment por meio de um GitHub App.
- [ ] Você não pode impedir autoavaliações, mas pode configurar alertas para ver quem acionou o deployment.
- [ ] Apenas usuários individuais podem ser atribuídos como revisores obrigatórios, não equipes.
> Tanto usuários individuais quanto equipes podem ser atribuídos como revisores obrigatórios
- [ ] Os revisores obrigatórios precisam de pelo menos acesso de `write` ao repositório para aprovar.
> Os revisores obrigatórios precisam de pelo menos acesso de `read`.
