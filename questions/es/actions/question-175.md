---
question: "Catherine escribe el siguiente job de workflow abajo. ¿Cuál será el resultado del job?"
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

- [x] El script de Python no se ejecutará, porque `actions/checkout` no está incluido en el workflow.
> `actions/checkout` es necesario para clonar el código del repositorio en el sistema de archivos del runner. Si no se utiliza, el script de Python no se encontrará y, por lo tanto, no se ejecutará.
- [ ] El script de Python se ejecutará exitosamente, porque el comando `chmod` otorga permisos de ejecución al script.
> Esto sería cierto si se usara `actions/checkout`.
- [ ] El script de Python no se ejecutará, porque `runs-on` no tiene un valor de `python`.
- [ ] El script de Python no se ejecutará, porque `actions/python-setup` no es la acción correcta para configurar Python.
> La mayoría de las acciones oficiales que configuran lenguajes de programación usan la estructura `actions/setup-<language>`.
