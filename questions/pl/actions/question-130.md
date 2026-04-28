---
question: "Które z poniższych stwierdzeń dotyczących bloków `outputs` na poziomie przepływu pracy i poziomie zadania są prawdziwe?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/workflow-syntax#example-defining-outputs-for-a-job"
---

- [ ] Bloki `outputs` na poziomie zadań powinny być używane tylko w przepływach pracy wywołujących, a nie wielokrotnego użytku.
> Przepływy pracy wielokrotnego użytku mogą zawierać zarówno bloki `outputs` na poziomie zadań, jak i na poziomie przepływu pracy.
- [x] Blok `outputs` na poziomie przepływu pracy powinien być używany tylko w przepływach pracy wielokrotnego użytku, a nie wywołujących.
> Blok `outputs` na poziomie przepływu pracy odnosi się do bloku `outputs`, który jest bezpośrednim dzieckiem `workflow_call` w przepływach pracy wielokrotnego użytku. W przepływach pracy niewielokrotnego użytku bloki `outputs` powinny występować wyłącznie na poziomie zadań.
- [x] Przepływ pracy wielokrotnego użytku może zawierać zarówno bloki `outputs` na poziomie przepływu pracy, jak i na poziomie zadań.
> Jeśli wymagane jest ustawienie wyjścia w przepływie pracy wielokrotnego użytku i przekazanie tego samego wyjścia do przepływu pracy wywołującego, należy użyć zarówno bloku `outputs` na poziomie przepływu pracy, jak i na poziomie zadań. 
> Więcej szczegółów można znaleźć w dokumentacji https://docs.github.com/en/actions/how-tos/reuse-automations/reuse-workflows#using-outputs-from-a-reusable-workflow
- [ ] Blok `outputs` na poziomie zadań musi mieć następującą strukturę:
```
outputs:
    <output-name>
        value: ${{ steps.<step-name>.outputs.<output-name> }}
```
> Blok `outputs` na poziomie zadań używa nienaznaczonej struktury par `key=value`. Więcej szczegółów znajduje się w oficjalnej dokumentacji (https://docs.github.com/en/actions/reference/workflows-and-actions/workflow-syntax#example-defining-outputs-for-a-job).
- [x] Blok `outputs` na poziomie przepływu pracy musi mieć następującą strukturę:
```
outputs:
    <output-name>
        value: ${{ jobs.<job-name>.outputs.<output-name> }}
```
> Blok `outputs` na poziomie przepływu pracy musi stosować powyższą strukturę. Klucz `value` jest zawsze wymagany. Opcjonalny klucz `description` również może być używany (nie widoczny w powyższym przykładzie).
> Więcej szczegółów znajduje się w dokumentacji - https://docs.github.com/en/actions/how-tos/reuse-automations/reuse-workflows#using-outputs-from-a-reusable-workflow
