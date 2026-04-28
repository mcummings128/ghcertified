---
question: "Jak możesz użyć GitHub API do utworzenia lub aktualizacji sekretu w repozytorium?"
documentation: "https://docs.github.com/en/rest/actions/secrets?create-or-update-a-repository-secret=&apiVersion=2022-11-28#create-or-update-a-repository-secret"
---

- [x] `PUT /repos/{owner}/{repo}/actions/secrets/{secret_name}`
- [ ] `POST /repos/{owner}/{repo}/actions/secrets/{secret_name}`
> `POST` nie jest poprawny dla tego endpointu. Tylko `PUT` może utworzyć lub zaktualizować sekrety w repozytorium.
- [ ] `HEAD /repos/{owner}/{repo}/actions/secrets/{secret_name}`
- [ ] `GET /repos/{owner}/{repo}/actions/secrets/{secret_name}`
