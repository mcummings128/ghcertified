---
question: "W jaki sposób można pobierać artefakty?"
documentation: "https://github.com/actions/upload-artifact#inputs"
---

- [x] Używając akcji `actions/download-artifact` w workflow 
- [x] Pobierając artefakty z interfejsu użytkownika GitHub Actions z poziomu uruchomienia workflow  
> Użycie interfejsu użytkownika umożliwia bezpośrednie pobieranie artefaktów. Zobacz [dokumentację](https://docs.github.com/en/actions/how-tos/manage-workflow-runs/download-workflow-artifacts), aby uzyskać więcej szczegółów.
- [x] Korzystając z określonego endpointu API GitHub
> API GitHub ma endpoint "Download an artifact". Zobacz [dokumentację](https://docs.github.com/en/rest/actions/artifacts?apiVersion=2026-03-10#download-an-artifact), aby uzyskać więcej szczegółów.
- [ ] Używając akcji `actions/upload-artifact` w workflow 
> `actions/upload-artifact` służy do przesyłania artefaktów, a nie do ich pobierania.
- [ ] Zdalnie uzyskując dostęp do self-hosted runners przez SSH i uzyskując dostęp do katalogu `.github/artifacts`
> Artefakty są zazwyczaj przechowywane z wykorzystaniem infrastruktury GitHub, a nie na runnerach. Jest jeden wyjątek: podczas używania GitHub Enterprise Server (GHES), artefakty i inne dane generowane przez uruchomienia workflow są przechowywane w zewnętrznej pamięci blob. Zobacz [dokumentację](https://docs.github.com/en/enterprise-server/admin/managing-github-actions-for-your-enterprise/getting-started-with-github-actions-for-your-enterprise/getting-started-with-github-actions-for-github-enterprise-server#external-storage-requirements), aby uzyskać więcej informacji na temat wymagań dotyczących przechowywania w GHES.
