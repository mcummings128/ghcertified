---
question: "Działania JavaScript i `actions/github-script` oba używają JavaScript. Dlaczego powinieneś używać `actions/github-script` zamiast tworzyć własne działanie w JavaScript?"
documentation: "https://github.com/actions/github-script"
---

- [x] `actions/github-script` powinien być używany do krótkich skryptów w linii.
- [x] `actions/github-script` powinien być używany, gdy chcesz korzystać z wstępnie uwierzytelnionego klienta do interakcji z GitHub API.
- [x] Działania JavaScript powinny być używane, gdy chcesz utworzyć niestandardowe działanie wielokrotnego użytku do użycia w różnych repozytoriach.
- [ ] Działania JavaScript powinny być używane do krótkich skryptów w linii.
- [ ] `actions/github-script` powinien być używany, gdy potrzebujesz precyzyjnie dostrojonego środowiska Node.js z kilkoma specyficznymi zależnościami.
> Chociaż możesz instalować moduły do użycia z `actions/github-script` przed jego wywołaniem, jeśli potrzebne są liczne zależności, prowadzi to do zwiększenia liczby kroków w workflow. `actions/github-script` również nie pozwala na zmianę wersji Node.js; jesteś związany tą, którą określa.
- [ ] Działania JavaScript powinny być używane, gdy chcesz niskonakładowego rozwiązania do wykonywania wywołań GitHub API.
> Działania JavaScript nie są niskonakładowe; wymagają stworzenia pliku `action.yml`, który z kolei musi być przechowywany w osobnym folderze, a nawet w osobnym repozytorium, w zależności od podejścia. `actions/github-script` zawiera wstępnie uwierzytelnionego klienta, co umożliwia łatwe wykonywanie wywołań GitHub API za pomocą podejścia opartego na JavaScript.
