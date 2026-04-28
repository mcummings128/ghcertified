---
question: "Które z poniższych stwierdzeń są prawdziwe w odniesieniu do wywoływania wielokrotnego użytku workflowów w porównaniu z wywoływaniem złożonych akcji?"
documentation: "https://docs.github.com/en/actions/concepts/workflows-and-actions/reusing-workflow-configurations#key-differences-between-reusable-workflows-and-composite-actions"
---

- [x] Złożone akcje są wywoływane poprzez odwołanie do folderu zawierającego plik `action.yml`.
> Jako akcja, złożone akcje muszą zawierać główną część swojej logiki w pliku `action.yml`. Aby wywołać złożoną akcję, należy wskazać lokalizację jej pliku `action.yml` (łącznie z katalogiem głównym, np. aby wywołać złożoną akcję znajdującą się w katalogu głównym tego samego repozytorium co workflow wywołujący, należy użyć składni `uses: ./`).
- [ ] Wielokrotnego użytku workflowy są wywoływane poprzez odwołanie do folderu zawierającego ich plik `action.yml`.
> Wielokrotnego użytku workflowy to zwykłe pliki `.yml` lub `.yaml`, które są przechowywane w katalogu `.github/workflows`. Nie posiadają pliku `action.yml`.
- [x] Złożone akcje muszą być wywoływane jako krok w ramach zadania.
> Złożone akcje (podobnie jak inne akcje) są wywoływane w kroku zadania workflowa — innymi słowy, nie potrzebujesz osobnego zadania workflowa tylko do wywołania złożonej akcji.
- [x] Wielokrotnego użytku workflowy muszą być wywoływane na poziomie zadania workflowa (nie z poziomu kroku).
> Kroki w ramach zadania workflowa nie mogą wywoływać workflowa wielokrotnego użytku. Workflow wielokrotnego użytku musi być wywoływany przez poszczególne zadanie w obrębie workflowa wywołującego. Może to powodować uruchamianie jednego lub więcej zadań w ramach workflowa wywołującego (zadania te można zobaczyć w widoku uruchomień workflowów w interfejsie użytkownika GitHub Actions).
- [ ] Sekrety mogą być przekazywane zarówno do wielokrotnego użytku workflowów, jak i złożonych akcji za pomocą bloku `uses.secrets`.
> Tylko workflowy wielokrotnego użytku mogą być wywoływane z użyciem bloku `secrets`. Aby przekazać sekrety do złożonej akcji, należy użyć obejść (takich jak przekazanie sekretu jako wejścia).
- [ ] Tylko workflowy wielokrotnego użytku mogą akceptować dane wejściowe.
> Zarówno workflowy wielokrotnego użytku, jak i złożone akcje mogą akceptować dane wejściowe.
- [x] Workflowy wielokrotnego użytku mogą używać innego typu agenta niż workflow wywołujący, podczas gdy złożone akcje nie mogą.
> Workflowy wielokrotnego użytku mają zadania jak każdy inny workflow, a te zadania mogą określać inny typ agenta za pomocą klucza `jobs.runs-on`. Złożone akcje dziedziczą środowisko agenta z workflowa wywołującego.
