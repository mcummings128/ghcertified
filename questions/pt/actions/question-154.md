---
question: "Quando você criaria uma ação de contêiner Docker para compartilhar no GitHub Actions marketplace?"
documentation: "https://docs.github.com/en/actions/concepts/workflows-and-actions/custom-actions#docker-container-actions"
---

- [x] As ações de contêiner Docker garantem um ambiente de runtime consistente e dependências específicas sem que os usuários precisem gerenciar esses aspectos por conta própria
- [ ] As ações de contêiner Docker são uma ação pronta para uso, com baixa sobrecarga
> As ações de contêiner Docker não são consideradas de baixa sobrecarga, pois exigem o uso de uma imagem (pré-construída ou especificada pelo `Dockerfile`), um script entrypoint e, possivelmente, lógica pré e pós-entrypoint.
- [ ] As ações de contêiner Docker têm inicialização rápida em runners Windows e macOS
> Os contêineres Docker só podem ser executados em runners de sistema operacional Linux (`ubuntu-latest` para runners hospedados no GitHub). Eles também demoram mais em comparação com as ações JavaScript e compostas.
- [ ] As ações de contêiner Docker são um conjunto de etapas dentro de outros fluxos de trabalho que são executados no contexto do fluxo/ação que as chama
> Um "conjunto reutilizável de etapas" descreve uma ação composta, não uma ação de contêiner Docker.
- [ ] As ações de contêiner Docker permitem usar Docker sem exigir um arquivo `action.yml`
> Todas as ações, independentemente do tipo, devem usar um arquivo `action.yml`.
