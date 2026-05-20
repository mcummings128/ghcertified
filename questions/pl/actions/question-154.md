---
question: "Kiedy należy zbudować akcję kontenera Docker do udostępnienia w GitHub Actions marketplace?"
documentation: "https://docs.github.com/en/actions/concepts/workflows-and-actions/custom-actions#docker-container-actions"
---

- [x] Akcje kontenerów Docker zapewniają spójne środowisko wykonawcze i specyficzne zależności, bez konieczności obsługi tych aspektów przez użytkowników
- [ ] Akcje kontenerów Docker to gotowe do użycia akcje o niskim narzucie
> Akcje kontenerów Docker nie są uważane za działania o niskim narzucie, ponieważ wymagają użycia obrazu (wstępnie zbudowanego lub określonego w pliku `Dockerfile`), skryptu punktu wejścia oraz potencjalnie logiki przed i po punkcie wejścia.
- [ ] Akcje kontenerów Docker charakteryzują się szybkim startem na runnerach Windows i macOS
> Kontenery Docker mogą być uruchamiane tylko na runnerach systemu Linux (np. `ubuntu-latest` w przypadku runnerów hostowanych przez GitHub). Uruchamianie kontenerów trwa dłużej w porównaniu do akcji JavaScript oraz złożonych akcji.
- [ ] Akcje kontenerów Docker to zestawy kroków w ramach innych przepływów pracy, które wykonywane są w kontekście wywołującego je workflow/akcji
> "Zestaw kroków wielokrotnego użytku" opisuje akcję złożoną, a nie akcję kontenera Docker.
- [ ] Akcje kontenerów Docker pozwalają na użycie Dockera bez konieczności posiadania pliku `action.yml`
> Wszystkie akcje, niezależnie od typu, muszą używać pliku `action.yml`.
