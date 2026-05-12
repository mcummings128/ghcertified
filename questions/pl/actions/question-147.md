---
question: "Masz sekret zakodowany w formacie base-64, który dekodujesz w przepływie pracy GitHub Actions. Jak możesz upewnić się, że zdekodowany sekret nie pojawi się przypadkowo w dzienniku przepływu pracy?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/workflow-commands#masking-a-value-in-a-log"
---

- [x] Użycie polecenia przepływu pracy `add-mask` w zadaniach, w których może być używany zdekodowany sekret.
> Użycie `add-mask` spowoduje ukrycie wartości, które GitHub Actions nie rozpoznaje jako sekret. Należy to zrobić raz dla każdej wartości, dla każdego zadania, które wykorzystuje zdekodowany sekret.
- [ ] Nie trzeba nic robić, ponieważ infrastruktura GitHub Actions automatycznie ukrywa zdekodowane sekrety.
> Nie ma gwarancji, że GitHub Actions będzie w stanie automatycznie wykryć i ukryć przekształcone sekrety zgodnie z [dokumentacją](https://docs.github.com/en/actions/reference/security/secure-use#use-secrets-for-sensitive-information).  
- [ ] Unikanie używania instrukcji drukowania, które zawierają zdekodowany sekret, ponieważ jest to jedyny sposób, w jaki zdekodowany sekret mógłby pojawić się w dzienniku przepływu pracy.
> Chociaż unikanie instrukcji drukowania zawierających zdekodowane sekrety jest zalecane, zdekodowane sekrety mogą pojawić się w innych miejscach w dzienniku przepływu pracy, takich jak komunikaty dotyczące wywołań API.
- [ ] Użycie wbudowanej funkcji `maskSecret`, aby ukryć zdekodowany sekret w miejscach, gdzie może być używany.
> `maskSecret` nie jest wbudowaną funkcją dostarczaną przez GitHub Actions.
