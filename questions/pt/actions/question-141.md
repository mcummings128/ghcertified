---
question: "Por que você pode usar `hashFiles` ao utilizar `actions/cache`?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/expressions#hashfiles"
---
```yaml
  - uses: actions/cache@v5
    with:
      path: ~/.npm
      key: ${{ runner.os }}-build-${{ env.cache-name }}-${{ hashFiles('**/package-lock.json') }}
```
- [x] Se uma chave de cache contém o arquivo de dependências envolvido em `hashFiles`, a chave muda quando o arquivo de dependências é atualizado, o que ajuda a mantê-lo atualizado.
> `hashFiles` é uma função integrada do GitHub que cria um hash do caminho especificado. Usá-lo para compor uma chave de cache faz com que o hash seja regenerado, atualizando assim a chave de cache. A documentação oficial [Referência de Cache de Dependências](https://docs.github.com/en/actions/reference/workflows-and-actions/dependency-caching#example-using-the-cache-action) mostra como usar `hashFiles` como parte de uma chave de cache.
- [ ] `hashFiles` é necessário para compatibilidade com runners do Windows.
- [ ] Ao usar `hashFiles` como parte de uma chave de cache, se houver um cache miss, `hashFiles` fornece informações adicionais de debug.  
- [ ] Ao usar `hashFiles` como parte de uma chave de cache, uma etapa adicional será gerada no workflow chamador. Essa etapa do workflow imprime o valor do hash SHA-256 da chave de cache para fins de referência.  
> Criar um hash da chave de cache não seria útil na maioria das situações.
