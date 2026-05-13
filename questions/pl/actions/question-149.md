---
question: "Co powoduje zapis do `GITHUB_STEP_SUMMARY`?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/workflow-commands#adding-a-job-summary"
---

```yaml
- name: "Zapisz wyniki zestawu testowego"
  run: |
    echo "Wyniki zestawu testowego to:" >> $GITHUB_STEP_SUMMARY
```
- [x] Dodaje tę linię do podsumowania zadania
> Zapis do `GITHUB_STEP_SUMMARY` dodaje dane do podsumowania zadania, które może być używane jako uproszczona wersja dziennika przebiegu działania.
- [ ] Dodaje tę linię jako podtytuł do nazwy kroku w interfejsie GitHub Actions
- [ ] Dodaje tę linię do wbudowanego artefaktu `github-steps-summary.md`
- [ ] Wypisuje tę linię jako komunikat debugowania na poziomie kroku
> Aby wypisać komunikat debugowania w kroku, musisz użyć składni `::debug::`. Zobacz sekcję "Setting a debug message" w podlinkowanej dokumentacji.
