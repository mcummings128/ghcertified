---
question: "Dlaczego warto używać `hashFiles` przy korzystaniu z `actions/cache`?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/expressions#hashfiles"
---
```yaml
  - uses: actions/cache@v5
    with:
      path: ~/.npm
      key: ${{ runner.os }}-build-${{ env.cache-name }}-${{ hashFiles('**/package-lock.json') }}
```
- [x] Jeśli klucz pamięci podręcznej zawiera plik zależności owinięty w `hashFiles`, klucz zmienia się, gdy plik zależności zostanie zaktualizowany, co pomaga utrzymać go w aktualnej wersji.
> `hashFiles` to wbudowana funkcja GitHub, która tworzy skrót określonej ścieżki. Użycie jej do stworzenia klucza pamięci podręcznej powoduje wygenerowanie nowego skrótu, co z kolei aktualizuje klucz pamięci podręcznej. Oficjalna dokumentacja [Dependency Caching Reference](https://docs.github.com/en/actions/reference/workflows-and-actions/dependency-caching#example-using-the-cache-action) pokazuje, jak używać `hashFiles` jako części klucza pamięci podręcznej.
- [ ] `hashFiles` jest wymagane dla kompatybilności z runnerami Windows.
- [ ] Gdy `hashFiles` jest używane jako część klucza pamięci podręcznej, w przypadku braku trafienia w pamięć podręczną, `hashFiles` dostarcza dodatkowych informacji debugowania.  
- [ ] Gdy `hashFiles` jest używane jako część klucza pamięci podręcznej, generowany jest dodatkowy krok w wywoływanym workflow. Ten krok workflow wyświetla wartość skrótu SHA-256 klucza pamięci podręcznej w celach referencyjnych.  
> Tworzenie skrótu klucza pamięci podręcznej nie byłoby użyteczne w większości sytuacji.
