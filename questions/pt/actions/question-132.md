---
question: "Quais das seguintes opções são verdadeiras a respeito do GitHub Enterprise Server (GHES)?"
documentation: "https://docs.github.com/en/enterprise-server/admin/overview/about-github-enterprise-server"
---

- [x] Os workflows do GHES não podem acessar o GitHub.com nem ações do GitHub Marketplace por padrão.
- [x] `actions/actions-sync` é principalmente dedicado a transferir ações do GitHub.com para uma instância do GHES.
> A sincronização de Actions do GitHub.com é realizada principalmente por meio do GitHub Connect ou do `actions-sync`. A ferramenta `actions/actions-sync` é uma [maneira manual](https://docs.github.com/en/enterprise-server/admin/managing-github-actions-for-your-enterprise/managing-access-to-actions-from-githubcom/manually-syncing-actions-from-githubcom) de realizar esse processo.
- [ ] O GHES tem permissão para usar versões avançadas de GitHub-hosted runners.
> O GHES não tem acesso aos GitHub-hosted runners. Isso é indicado na documentação do [`actions/actions-sync`](https://docs.github.com/en/enterprise-server/admin/managing-github-actions-for-your-enterprise/managing-access-to-actions-from-githubcom/manually-syncing-actions-from-githubcom).
- [ ] Usando o GitHub Connect, os usuários podem seguir um processo manual para acessar as ações do GitHub.com. Esse processo deve ser realizado uma vez para cada ação desejada.
> O GitHub Connect permite acesso automático às ações do GitHub.com. Os usuários devem seguir um processo de configuração, mas geralmente isso só precisa ser feito uma vez. Consulte a [documentação do GitHub Connect](https://docs.github.com/en/enterprise-server/admin/managing-github-actions-for-your-enterprise/managing-access-to-actions-from-githubcom/enabling-automatic-access-to-public-githubcom-actions-using-github-connect#enabling-automatic-access-to-public-githubcom-actions) para mais detalhes.
- [x] As instâncias do GitHub Enterprise Server são auto-hospedadas, comparadas ao GitHub Enterprise Cloud (GHEC), que é hospedado e gerenciado pelo GitHub.
> [GitHub Enterprise Server](https://docs.github.com/en/enterprise-server/admin/overview/about-github-enterprise-server) é uma versão auto-hospedada da plataforma GitHub. [GitHub Enterprise Cloud](https://docs.github.com/en/enterprise-cloud@latest/admin/overview/about-github-enterprise-cloud) é hospedado em um subdomínio dedicado do GHE.com. Todos os subdomínios do GHE.com são hospedados pelo GitHub.
