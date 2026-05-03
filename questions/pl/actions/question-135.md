---
question: "Sklonowałeś repozytorium, aby ulepszyć przepływ pracy korzystający z sekretu do uzyskania dostępu do aplikacji zewnętrznej. Uruchamiasz przepływ pracy przed edycją jego kodu, aby uzyskać wynik bazowy, ale okazuje się, że przepływ pracy się nie powiódł. Dlaczego mogło się tak stać?"
documentation: "https://docs.github.com/en/actions/how-tos/write-workflows/choose-what-workflows-do/use-secrets?tool=webui#using-secrets-in-a-workflow"
---

- [x] Sklonowane repozytoria nie dziedziczą sekretów z oryginalnego repozytorium  
> Ze względów bezpieczeństwa (z wyjątkiem `GITHUB_TOKEN`) sekrety nie są przekazywane do runnera, gdy przepływ pracy jest uruchamiany z poziomu sklonowanego repozytorium. Spowoduje to niepowodzenie przepływu pracy, jeśli odwołuje się on do sekretu z oryginalnego repozytorium.
- [ ] Podczas dziedziczenia sekretu z oryginalnego repozytorium wystąpił błąd podczas klonowania, co spowodowało uszkodzenie lub nieważność sekretu  
> Z wyjątkiem `GITHUB_TOKEN`, sekrety nie są przekazywane do runnera, gdy przepływ pracy jest uruchamiany z poziomu sklonowanego repozytorium. Z tego powodu nie mogło wystąpić takie uszkodzenie.
- [ ] Dziedziczony sekret miał rozmiar większy niż 48 KB  
> Z wyjątkiem `GITHUB_TOKEN`, sekrety nie są przekazywane do runnera, gdy przepływ pracy jest uruchamiany z poziomu sklonowanego repozytorium. Dlatego rozmiar nie ma tutaj znaczenia.
- [ ] Sklonowane repozytoria dziedziczą tylko sekrety repozytorium, więc sekret używany w przepływie pracy musiał być sekretem organizacyjnym lub środowiskowym.  
> Z wyjątkiem `GITHUB_TOKEN`, sekrety nie są przekazywane do runnera, gdy przepływ pracy jest uruchamiany z poziomu sklonowanego repozytorium. Dotyczy to wszystkich typów sekretów (repozytorium, środowiskowych i organizacyjnych).
