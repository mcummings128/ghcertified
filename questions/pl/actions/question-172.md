---
question: "Ingrid chce, aby jej organizacja mogła korzystać z grupy samodzielnie hostowanych Linux runners tylko w określonych repozytoriach. Jaki jest najlepszy sposób, aby zapewnić takie zachowanie?"
documentation: "https://docs.github.com/en/actions/how-tos/manage-runners/self-hosted-runners/manage-access#changing-which-repositories-can-access-a-runner-group"
---

- [x] Utwórz nową grupę runnerów, dodaj runnery do grupy, a następnie w ustawieniach grupy wybierz, które repozytoria mają mieć dostęp do grupy.
- [ ] Utwórz nową etykietę runnera, przypisz etykiety do runnerów, a następnie wybierz, które repozytoria mają mieć dostęp do etykiety w ustawieniach etykiety.
- [ ] Utwórz nową etykietę runnera, przypisz etykiety do runnerów, a następnie upewnij się, że wszystkie workflowy w repozytoriach zawierają tę etykietę w polu `runs-on`.
> Etykiety nie ograniczają dostępu do runnerów. Samo dodanie etykiety nie wystarczy; dodanie etykiet do `runs-on` może potencjalnie spowodować, że odpowiedni workflow znajdzie runner, na którym może się uruchomić.
- [ ] Utwórz nową grupę runnerów, wybierz "Linux" jako system operacyjny i użyj wzorców glob do określenia, które repozytoria mają mieć dostęp w ustawieniach grupy.
