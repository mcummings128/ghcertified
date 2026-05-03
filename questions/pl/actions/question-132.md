---
question: "Które z poniższych stwierdzeń dotyczących GitHub Enterprise Server (GHES) są prawdziwe?"
documentation: "https://docs.github.com/en/enterprise-server/admin/overview/about-github-enterprise-server"
---

- [x] Domyślnie przepływy pracy GHES nie mają dostępu do GitHub.com ani do akcji z GitHub Marketplace. 
- [x] `actions/actions-sync` jest głównie przeznaczony do przenoszenia akcji z GitHub.com do instancji GHES.
> Synchronizacja akcji z GitHub.com jest głównie realizowana za pomocą GitHub Connect lub `actions-sync`. Narzędzie `actions/actions-sync` to [ręczny sposób](https://docs.github.com/en/enterprise-server/admin/managing-github-actions-for-your-enterprise/managing-access-to-actions-from-githubcom/manually-syncing-actions-from-githubcom) na wykonanie tego procesu. 
- [ ] GHES może korzystać z ulepszonych wersji runnerów hostowanych przez GitHub.
> GHES w ogóle nie ma dostępu do runnerów hostowanych przez GitHub. Jest to opisane w dokumentacji [`actions/actions-sync`](https://docs.github.com/en/enterprise-server/admin/managing-github-actions-for-your-enterprise/managing-access-to-actions-from-githubcom/manually-syncing-actions-from-githubcom).
- [ ] Korzystając z GitHub Connect, użytkownicy mogą ręcznie uzyskać dostęp do akcji GitHub.com. Proces ten musi być przeprowadzony dla każdej żądanej akcji.
> GitHub Connect umożliwia automatyczny dostęp do akcji GitHub.com. Użytkownicy muszą przeprowadzić proces konfiguracji, ale zazwyczaj odbywa się to tylko raz. Szczegóły znajdują się w [dokumentacji GitHub Connect](https://docs.github.com/en/enterprise-server/admin/managing-github-actions-for-your-enterprise/managing-access-to-actions-from-githubcom/enabling-automatic-access-to-githubcom-actions-using-github-connect#enabling-automatic-access-to-public-githubcom-actions).
- [x] Instancje GitHub Enterprise Server są hostowane lokalnie, w przeciwieństwie do GitHub Enterprise Cloud (GHEC), który jest hostowany i zarządzany przez GitHub.
> [GitHub Enterprise Server](https://docs.github.com/en/enterprise-server/admin/overview/about-github-enterprise-server) to wersja platformy GitHub hostowana lokalnie. Instancje [GitHub Enterprise Cloud](https://docs.github.com/en/enterprise-cloud@latest/admin/overview/about-github-enterprise-cloud) są hostowane w dedykowanej subdomenie GHE.com. Wszystkie subdomeny GHE.com są hostowane przez GitHub.
