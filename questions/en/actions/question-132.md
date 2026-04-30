---
question: "Which of the following are true regarding Github Enterprise Server (GHES)?"
documentation: "https://docs.github.com/en/enterprise-server/admin/overview/about-github-enterprise-server"
---

- [x] GHES workflows cannot access Github.com nor Github Marketplace actions by default. 
- [x] `actions/actions-sync` is primarily devoted to move Github.com actions to a GHES instance.
> Syncing Actions from Github.com is mainly accomplished either via Github Connect or `actions-sync`. The `actions/actions-sync` tool is a [manual way](https://docs.github.com/en/enterprise-server@3.14/admin/managing-github-actions-for-your-enterprise/managing-access-to-actions-from-githubcom/manually-syncing-actions-from-githubcom) to perform this process. 
- [ ] GHES is allowed to use enhanced versions of Github-hosted runners.
> GHES does not have access to Github-hosted runners at all. This is seen in the [`actions/actions-sync` documentation](https://docs.github.com/en/enterprise-server@3.14/admin/managing-github-actions-for-your-enterprise/managing-access-to-actions-from-githubcom/manually-syncing-actions-from-githubcom)
- [ ] Using Github Connect, users can follow a manual process to access Github.com actions. This process must be done once per desired action.
> Github Connect allows automatic access to Github.com actions. Users must follow a setup process, but this generally only needs to be done once. See the [Github Connect documentation](https://docs.github.com/en/enterprise-server@3.14/admin/managing-github-actions-for-your-enterprise/managing-access-to-actions-from-githubcom/enabling-automatic-access-to-githubcom-actions-using-github-connect#enabling-automatic-access-to-public-githubcom-actions) for more details.
- [x] Github Enterprise Server instances are self-hosted, compared to Github Enterprise Cloud (GHEC) which is hosted and managed by Github.
> [GitHub Enterprise Server](https://docs.github.com/en/enterprise-server@3.15/admin/overview/about-github-enterprise-server) is a self-hosted version of the GitHub platform. [Github Enterprise Cloud](https://docs.github.com/en/enterprise-cloud@latest/admin/overview/about-github-enterprise-cloud) instances are hosted on a dedicated subdomain of GHE.com. All GHE.com subdomains are hosted by Github.