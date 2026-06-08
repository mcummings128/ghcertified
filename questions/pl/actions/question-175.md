---
question: "Catherine pisze poniższy kod dla zadania workflow. Jaki będzie wynik działania tego zadania?"
documentation: "https://github.com/actions/checkout"
---

```yaml
jobs:
  doc-generate:
    name: "Generate Scaffold Doc"
    runs-on: ubuntu-latest
    steps:
      
      - name: Setup Python 3.13 
        uses: actions/setup-python@v6
        with:
          python-version: '3.13' 

      - name: Grant Execute Permission to Scaffolding Python Script
        run: chmod +x ./scripts/scaffold-doc.py

      - name: Execute Scaffolding Python Script
        run: python ./scripts/scaffold-doc.py
```

- [x] Skrypt Python nie zostanie uruchomiony, ponieważ `actions/checkout` nie jest uwzględnione w workflow.
> `actions/checkout` jest niezbędne do pobrania kodu repozytorium do systemu plików runnera. Jeśli nie zostanie użyte, skrypt Python nie zostanie znaleziony i w efekcie nie zostanie uruchomiony.
- [ ] Skrypt Python zostanie uruchomiony pomyślnie, ponieważ polecenie `chmod` nadaje uprawnienia do wykonywania skryptu.
> To byłoby prawdą, gdyby `actions/checkout` zostało użyte.
- [ ] Skrypt Python nie zostanie uruchomiony, ponieważ `runs-on` nie ma wartości `python`.
- [ ] Skrypt Python nie zostanie uruchomiony, ponieważ `actions/python-setup` nie jest właściwą akcją do konfiguracji Pythona.
> Większość oficjalnych akcji, które konfigurują języki programowania, korzysta ze struktury `actions/setup-<language>`. 
