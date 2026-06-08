---
question: "Zaobserwuj wartości w kluczu `runs-on`, jak pokazano w poniższym zadaniu workflow. Co jest prawdą w kontekście sposobu, w jaki zadanie zostanie uruchomione?"
documentation: "https://docs.github.com/en/actions/how-tos/manage-runners/self-hosted-runners/use-in-a-workflow#using-custom-labels-to-route-jobs"
---
```yaml
jobs:
    fire_emblem_deploy:
        name: "Deploy the 'Fire Emblem' application"
        runs-on: [self-hosted,nes,linux]
```

- [x] Zadanie zostanie uruchomione na self-hosted runnerze, który ma zastosowane wszystkie etykiety.
- [ ] Zadanie zostanie uruchomione na self-hosted runnerze, który ma zastosowaną dowolną z etykiet.
> Etykiety runnerów są stosowane kumulatywnie; workflow nie zostanie uruchomiony na runnerze, który ma tylko niektóre z etykiet. Wszystkie muszą być obecne.
- [ ] Zadanie nadal będzie mogło zostać uruchomione na GitHub-hosted runnerach, ponieważ mogą mieć zastosowane niestandardowe etykiety.
> GitHub-hosted runnery nie mogą mieć zastosowanych niestandardowych etykiet. Muszą być odwoływane za pomocą [zdefiniowanych etykiet](https://docs.github.com/en/enterprise-cloud@latest/actions/how-tos/write-workflows/choose-where-workflows-run/choose-the-runner-for-a-job#standard-github-hosted-runners-for-public-repositories), które zostały im przypisane.
- [ ] Zadanie zostanie uruchomione na runnerze (self-hosted lub GitHub-hosted, w zależności od tego, który będzie dostępny jako pierwszy) o nazwie `self-hosted,nes,linux`.
> `runs-on` odnosi się do etykiet runnerów, a nie nazw.
