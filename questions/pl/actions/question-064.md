---
question: "Jak organizacje korzystające z GitHub Enterprise Server mogą włączyć automatyczną synchronizację zewnętrznych GitHub Actions hostowanych na GitHub.com z ich instancją GitHub Enterprise Server?"
documentation: "https://docs.github.com/en/enterprise-server@3.17/admin/github-actions/managing-access-to-actions-from-githubcom/enabling-automatic-access-to-githubcom-actions-using-github-connect"
---

- [x] Korzystając z GitHub Connect
> Po włączeniu GitHub Connect automatycznie nawiązuje bezpieczne połączenie między instancją GitHub Enterprise Server (GHES) a kontem GitHub Enterprise Cloud (GHEC) (GHEC jest hostowane na GitHub.com). Konto GHEC służy jako zaufana (uwierzytelniona) tożsamość, którą GitHub.com wykorzystuje do autoryzacji instancji GHES w celu uzyskania dostępu do akcji hostowanych na GitHub.com.   
- [ ] GitHub Enterprise Server ma dostęp do wszystkich GitHub.com Actions domyślnie
> GitHub Actions na GitHub Enterprise Server zostało zaprojektowane do pracy w środowiskach bez pełnego dostępu do Internetu. Domyślnie workflowy nie mogą korzystać z akcji z GitHub.com ani GitHub Marketplace.
- [ ] Korzystając z narzędzia actions-sync
> Chociaż narzędzie actions-sync może być używane do synchronizowania pojedynczych repozytoriów akcji z GitHub.com w przedsiębiorstwie, jest to podejście ręczne. Zobacz [dokumentację](https://docs.github.com/en/enterprise-server@3.17/admin/github-actions/managing-access-to-actions-from-githubcom/manually-syncing-actions-from-githubcom#about-the-actions-sync-tool) po więcej szczegółów.
- [ ] GitHub Enterprise Server (GHES) nie może korzystać z GitHub.com Actions ze względu na jego lokalny charakter i brak dostępu do internetu.
> Chociaż workflowy znajdujące się w instancji GHES domyślnie nie mogą korzystać z GitHub.com Actions ani z akcji GitHub Marketplace, można to naprawić za pomocą GitHub Connect lub actions-sync.
