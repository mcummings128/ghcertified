---
question: "Marianne ma gałąź funkcji, która zawiera jej nowy plik workflow, ustawiony do uruchamiania codziennie o 2:00, przy użyciu składni przedstawionej poniżej. Jednak następnego dnia workflow nie uruchamia się. Jaka może być tego przyczyna?"
documentation: "https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows#schedule"
---

```yaml
on:
    schedule:
        cron:
            "0 2 * * *"
```

- [x] Plik workflow musi znajdować się w domyślnej gałęzi, aby mógł być wyzwalany przez zdarzenie `schedule`
- [ ] Składnia `cron` nie jest prawidłowo zaplanowana
> `"0 2 * * *"` w składni CRON oznacza "uruchamianie codziennie o 2:00." Nawet jeśli harmonogram byłby ustawiony nieprawidłowo, workflow i tak nie zostałby uruchomiony, ponieważ nie znajduje się w domyślnej gałęzi.
- [ ] `schedule` nie może być jedynym zdarzeniem w workflow. Musi być połączone ze zdarzeniem opartym na repozytorium, takim jak `push`
- [ ] Nie użyto składni `@daily`
> Nietypowa składnia CRON, taka jak `@daily`, nie jest obsługiwana przez GitHub Actions. 
- [ ] Prywatne repozytorium zawierające workflow nie miało żadnej aktywności w ciągu ostatnich 60 dni, co automatycznie wyłącza workflow.
> To automatyczne wyłączanie dotyczy jedynie repozytoriów publicznych, a nie prywatnych.
