---
question: "¿Cómo te aseguras de que el paso `Upload Failure test report` se ejecute solo si el paso `Run Tests` falla?"
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
> `failure()` sobrescribe la verificación de estado predeterminada `success()` para que el paso pueda ejecutarse después de un fallo, y la verificación de resultado apunta al paso específico.

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
> `always()` funciona pero ejecuta el paso incluso en caso de cancelación, lo cual es más amplio de lo necesario.

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
> Sin una función de verificación de estado como `failure()`, se aplica implícitamente `success()`, por lo que este paso se omite después de un fallo, incluso si la verificación de resultado es correcta.

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
> No hay ninguna condición `if` — este paso solo se ejecuta cuando todos los pasos anteriores tienen éxito (el comportamiento predeterminado).
