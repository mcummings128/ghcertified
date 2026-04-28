---
question: "Który sposób uruchamiania zadania jest poprawny, jeśli zmienna konfiguracyjna `MY_VAR` ma wartość `MY_VALUE`?"
documentation: "https://docs.github.com/en/actions/learn-github-actions/contexts#example-usage-of-the-vars-context"
---

- [x] Poprzez tworzenie następującego warunku na poziomie zadania
```yaml
my-job:
  if: ${{ vars.MY_VAR == 'MY_VALUE' }}
```
- [ ] Poprzez tworzenie następującego warunku na poziomie zadania
```yaml
my-job:
  if: ${{ vars.MY_VAR }} == 'MY_VALUE'
```
> Niepoprawne, tylko `vars.MY_VAR` jest oceniane wewnątrz `${{ }}`; to powoduje tekst taki jak `some_value == 'MY_VALUE'`, a GitHub traktuje ten niepusty ciąg jako prawdziwy zamiast wykonywać porównanie
> Zobacz https://docs.github.com/en/actions/reference/workflows-and-actions/expressions#literals
- [ ] To nie jest możliwe, ponieważ zmiennych konfiguracyjnych nie można używać w warunkach `if`
> To prawda w przypadku `secrets`, ale nie dla zmiennych konfiguracyjnych
- [ ] To nie jest możliwe, ponieważ zmiennych konfiguracyjnych nie można używać w warunkach `if` na poziomie zadania
> To prawda w przypadku `secrets`, ale nie dla zmiennych konfiguracyjnych
