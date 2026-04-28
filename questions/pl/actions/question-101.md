---
question: "Jak zapewnić, aby krok `Upload Failure test report` był wykonywany tylko wtedy, gdy krok `Run Tests` zakończy się niepowodzeniem?"
documentation: "https://docs.github.com/en/actions/learn-github-actions/expressions#status-check-functions"
---

- [x] 
```yaml
- name: Run Tests
  id: run-tests
  run: npm run test

- name: Upload Failure test report
  if: failure() && steps.run-tests.outcome == 'failure'
  uses: actions/upload-artifact@v3
  with:
    name: test-report
    path: test-reports.html
```
> `failure()` zastępuje domyślną kontrolę statusu `success()`, dzięki czemu krok może być wykonany po niepowodzeniu, a warunek `outcome` odnosi się do konkretnego kroku.

- [ ] 
```yaml
- name: Run Tests
  id: run-tests
  run: npm run test

- name: Upload Failure test report
  if: always()
  uses: actions/upload-artifact@v3
  with:
    name: test-report
    path: test-reports.html
```
> `always()` działa, ale powoduje wykonanie kroku nawet w przypadku anulowania, co jest szerszym zakresem niż wymagane.

- [ ] 
```yaml
- name: Run Tests
  id: run-tests
  run: npm run test

- name: Upload Failure test report
  if: steps.run-tests.outcome == 'failure'
  uses: actions/upload-artifact@v3
  with:
    name: test-report
    path: test-reports.html
```
> Bez funkcji sprawdzania statusu, takiej jak `failure()`, domyślnie stosowana jest funkcja `success()`, więc ten krok jest pomijany po niepowodzeniu, nawet jeśli warunek `outcome` jest poprawny.

- [ ] 
```yaml
- name: Run Tests
  id: run-tests
  run: npm run test

- name: Upload Failure test report
  uses: actions/upload-artifact@v3
  with:
    name: test-report
    path: test-reports.html
```
> Brak warunku `if` — ten krok jest wykonywany tylko wtedy, gdy wszystkie poprzednie kroki zakończą się sukcesem (domyślne zachowanie).
