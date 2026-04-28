---
question: "「`Upload Failure test report` ステップを `Run Tests` ステップが失敗した場合にのみ実行するようにするにはどうすればよいですか？」"
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
> `failure()` はデフォルトの `success()` ステータスチェックを上書きして、失敗後にステップが実行できるようにします。また、outcome チェックは特定のステップを対象としています。

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
> `always()` は機能しますが、このステップは中断時にも実行されるため、必要以上に広範な条件となっています。

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
> `failure()` のようなステータスチェック機能を使用しない場合、暗黙的に `success()` が適用されるため、outcome チェックが正しいにもかかわらず、このステップは失敗後にスキップされます。

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
> `if` 条件がまったくない場合、このステップはデフォルトの動作として、すべての前のステップが成功した場合にのみ実行されます。
