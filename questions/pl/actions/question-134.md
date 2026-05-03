---
question: "Jak uruchomić niestandardowe skrypty JavaScript bezpośrednio w przepływie pracy GitHub Actions?"
documentation: "https://github.com/marketplace/actions/github-script"
---

- [x] Za pomocą akcji `actions/github-script`
> `actions/github-script` pozwala pisać i wykorzystywać wbudowany kod JavaScript w celu wykonywania wywołań API i uzyskiwania dostępu do kontekstu przepływu pracy. Aby użyć `actions/github-script`, należy ją wywołać jak każdą inną akcję, jak opisano w [dokumentacji](https://github.com/actions/github-script) 
- [ ] Włączając konfigurację „Allow custom JavaScript scripts” w ustawieniach Actions w repozytorium
> W ustawieniach Actions w repozytorium nie istnieje konfiguracja „Allow custom JavaScript scripts”.
- [ ] Włączając konfigurację „Allow custom JavaScript scripts” w ustawieniach Actions w organizacji
> W ustawieniach Actions w repozytorium nie istnieje konfiguracja „Allow custom JavaScript scripts”. Chociaż w ustawieniach Actions organizacji może być wymagane włączenie opcji takich jak „Allow actions created by Github” w celu używania oficjalnych akcji GitHub, nie dotyczy to wyłącznie `actions/github-script`.
- [ ] Zapisując treść bloku skryptu w zmiennej środowiskowej `GITHUB_SCRIPT`
> `GITHUB_SCRIPT` nie jest domyślną zmienną środowiskową GitHub Actions. Lista domyślnych zmiennych środowiskowych znajduje się w [dokumentacji](https://docs.github.com/en/actions/reference/workflows-and-actions/variables)
- [ ] W akcji JavaScript ustawiając klucz `using` na `'github-script'`
> Akcje JavaScript muszą mieć klucz `using` ustawiony na `node*`, gdzie * oznacza obsługiwaną wersję Node.js. Generalnie akcje JavaScript nie wymagają używania `actions/github-script`.
