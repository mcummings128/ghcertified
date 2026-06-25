---
question: "Musisz upewnić się, że środowisko `prod` wymaga ręcznego zatwierdzenia, zanim wdrożenia będą mogły być kontynuowane. Które z poniższych opcji są prawdziwe w kontekście konfiguracji tego ustawienia?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/deployments-and-environments#required-reviewers"
---

- [x] Jeśli wymienisz wymaganych recenzentów, tylko jeden z nich musi zatwierdzić, aby kontynuować wdrażanie.
- [x] Możesz zapobiec autoryzacji własnych recenzji w przypadku, gdy osoba, która chce wdrożyć, jest również wymagana jako recenzent.
- [ ] Jeśli wymienisz wymaganych recenzentów, wszyscy muszą zatwierdzić, aby kontynuować wdrażanie.
> Zaskakująco tylko 1 z wymaganych recenzentów musi zatwierdzić zadanie w ramach przepływu pracy. Aby wymusić takie zachowanie, musisz utworzyć niestandardową regułę ochrony wdrożeń za pomocą aplikacji GitHub App.
- [ ] Nie możesz zapobiec autoryzacji własnych recenzji, ale możesz skonfigurować alerty informujące, kto uruchomił wdrożenie.
- [ ] Wymaganymi recenzentami mogą być jedynie pojedynczy użytkownicy, a nie zespoły.
> Wymaganymi recenzentami mogą być zarówno pojedynczy użytkownicy, jak i zespoły.
- [ ] Wymagani recenzenci muszą mieć co najmniej dostęp na poziomie `write` do repozytorium, aby zatwierdzić.
> Wymagani recenzenci muszą mieć co najmniej dostęp na poziomie `read`.
