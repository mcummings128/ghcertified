---
question: "Twój workflow musi być uruchamiany o 12:00 w nocy w każdy poniedziałek i piątek. Który z poniższych fragmentów kodu odpowiada temu zachowaniu?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#schedule"
---

- [x] 
```yaml
on:
  schedule:
    - cron: '0 0 * * 1,5'
```
> Składnia `cron` ma swoje elementy zdefiniowane w kolejności rosnącej wielkości, z wyjątkiem elementu "dni tygodnia", który jest ostatnim elementem. Zobacz [dokumentację](https://pubs.opengroup.org/onlinepubs/9699919799/utilities/crontab.html#tag_20_25_07), aby uzyskać więcej informacji i przykładów.

- [ ] 
```yaml
on:
  schedule:
    - cron: '0 12 * * Mon,Fri'
```
> Element "dni tygodnia" musi być w formacie liczbowym. Dodatkowo elementy "minuty" i "godziny" wskazują na 12:00 w południe, a nie 12:00 w nocy.

- [ ] 
```yaml
on:
  workflow_schedule:
    - cron: '0 0 * * 1,5'
```

- [ ] 
```yaml
on:
  workflow_schedule:
    - cron: '1,5 * * 0 0'
```

- [ ] 
```yaml
on:
  workflow_call:
    - days: [Mon,Fri]
    - times: [00]
```
