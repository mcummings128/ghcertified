---
question: "De que maneiras você pode baixar um artifact?"
documentation: "https://github.com/actions/upload-artifact#inputs"
---

- [x] Usando a ação `actions/download-artifact` em um workflow 
- [x] Baixando artifacts a partir da execução do workflow na interface do GitHub Actions
> Usar a interface permite uma abordagem prática para baixar artifacts. Veja a [documentação](https://docs.github.com/en/actions/how-tos/manage-workflow-runs/download-workflow-artifacts) para mais detalhes.
- [x] Usando um endpoint específico da API do GitHub
> A API do GitHub possui um endpoint "Download an artifact". Veja a [documentação](https://docs.github.com/en/rest/actions/artifacts?apiVersion=2026-03-10#download-an-artifact) para mais detalhes.
- [ ] Usando a ação `actions/upload-artifact` em um workflow
> `actions/upload-artifact` é utilizado para fazer upload de artifacts, não para baixá-los.
- [ ] Acessando remotamente runners auto-hospedados via SSH e acessando o diretório `.github/artifacts`
> Os artifacts geralmente são armazenados usando a infraestrutura do GitHub, não pelos runners. Há uma exceção: ao usar o GitHub Enterprise Server (GHES), os artifacts e outros dados gerados por execuções de workflow são armazenados em um armazenamento externo de blobs. Veja a [documentação](https://docs.github.com/en/enterprise-server/admin/managing-github-actions-for-your-enterprise/getting-started-with-github-actions-for-your-enterprise/getting-started-with-github-actions-for-github-enterprise-server#external-storage-requirements) para mais detalhes sobre os requisitos de armazenamento do GHES.
