---
question: "Annette musi napisać workflow, aby opublikować niestandardowy pakiet `npm`, który będzie używany wyłącznie przez członków jej prywatnej organizacji. Co powinno znaleźć się w jej workflow?"
documentation: "https://docs.github.com/en/packages/learn-github-packages/publishing-a-package"
---

- [x] Logika publikowania w GitHub Packages
> GitHub Packages to rejestr pakietów zintegrowany z GitHub, co ułatwia jego używanie, jeśli Twoje potrzeby są specyficzne dla GitHuba (takie jak w przypadku actions/workflows). GitHub Packages umożliwia także prywatne hostowanie pakietów.
- [x] Token z uprawnieniami `write:packages`
> Tokeny dostępu osobistego są obsługiwane we wszystkich rejestrach pakietów GitHub Packages. Niektóre rejestry obsługują również użycie `GITHUB_TOKEN`. Więcej informacji znajdziesz w [dokumentacji](https://docs.github.com/en/packages/learn-github-packages/about-permissions-for-github-packages#about-scopes-and-permissions-for-package-registries).  
- [x] Logika komunikacji z odpowiednim rejestrem GitHub Packages `https://npm.pkg.github.com`
> Workflows związane z GitHub Packages często wymagają komunikacji z odpowiednim rejestrem pakietów hostowanym na GitHub, którego URL ma składnię `https://<package-type>.pkg.github.com`. Przykład znajdziesz w [dokumentacji rejestru npm](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-npm-registry).
- [ ] Zdarzenie `on:registry_package` bez określonych typów aktywności
> `on:registry_package` jest związane z pakietami, ale workflow nie wymaga tego zdarzenia do publikowania pakietu.
- [ ] Token z uprawnieniami `admin:packages`
> Uprawnienia `admin:packages` są wymagane tylko wtedy, gdy trzeba usunąć pakiet hostowany w GitHub Packages. Należy stosować zasadę najmniejszych uprawnień; w tym przypadku wystarczą uprawnienia `write`.
- [ ] Zdarzenie `on:registry_package` z `types:[published]`
> Zdarzenie `on:registry_package` może zostać skonfigurowane tak, aby uruchamiało workflow po opublikowaniu pakietu, ale workflow nie wymaga tego zdarzenia do opublikowania pakietu.
