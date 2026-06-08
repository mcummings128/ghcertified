---
question: "Jak uruchomić niestandardowe skrypty JavaScript bezpośrednio w workflow GitHub Actions?"
documentation: "https://github.com/marketplace/actions/github-script"
---

- [x] Za pomocą akcji `actions/github-script`
> `actions/github-script` umożliwia pisanie i używanie wbudowanego kodu JavaScript do wywoływania API oraz dostępu do kontekstu workflow. Aby użyć `actions/github-script`, należy wywołać ją jak każdą inną akcję, zgodnie z instrukcjami w [dokumentacji](https://github.com/actions/github-script).
- [ ] Poprzez włączenie konfiguracji „Allow custom JavaScript scripts” w ustawieniach Actions dla repozytorium
> Nie istnieje konfiguracja „Allow custom JavaScript scripts” w ustawieniach Actions dla repozytorium.
- [ ] Poprzez włączenie konfiguracji „Allow custom JavaScript scripts” w ustawieniach Actions organizacji
> Nie istnieje konfiguracja „Allow custom JavaScript scripts” w ustawieniach Actions dla repozytorium. Choć być może trzeba włączyć ustawienia takie jak „Allow actions created by GitHub” w ustawieniach Actions organizacji, aby korzystać z oficjalnych GitHub Actions, nie dotyczy to wyłącznie `actions/github-script`.
- [ ] Pisząc zawartość bloku skryptowego do zmiennej środowiskowej `GITHUB_SCRIPT`
> `GITHUB_SCRIPT` nie jest domyślną zmienną środowiskową w GitHub Actions. Lista domyślnych zmiennych środowiskowych znajduje się w [dokumentacji](https://docs.github.com/en/actions/reference/workflows-and-actions/variables).
- [ ] W JavaScript Action ustaw klucz `using` na wartość `'github-script'`
> JavaScript Actions musi mieć ustawiony klucz `using` na `node*`, gdzie `*` to wspierana wersja Node.js. Ogólnie rzecz biorąc, JavaScript Actions nie wymagają użycia `actions/github-script`.
