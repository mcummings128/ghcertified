---
question: "Mercedes chce opublikować działanie kontenerowe Docker, które stworzyła, w GitHub Actions Marketplace. Jakie pliki są jej minimalnie potrzebne, aby to zrobić?"
documentation: "https://docs.github.com/en/actions/how-tos/create-and-publish-actions/publish-in-github-marketplace"
---

- [x] `action.yml`
> Plik `action.yml` jest wymagany, aby działanie mogło zostać opublikowane w Marketplace, niezależnie od jego rodzaju.
- [x] `Dockerfile`, jeśli obraz jest tworzony jako część działania podczas uruchamiania workflow
> Działania kontenerowe Docker wymagają `Dockerfile` tylko wtedy, gdy obraz musi być tworzony od podstaw i nie można go pobrać z rejestru obrazów. Wartość `runs.image` w `action.yml` musi być ścieżką do `Dockerfile`.
- [ ] `Dockerfile`, jeśli obraz ma być odwoływany z rejestru obrazów
> Podczas odwoływania się do obrazu w rejestrze obrazów, plik `Dockerfile` nie jest potrzebny. Wartość klucza `runs.image` w `action.yml` musi być poprzedzona `docker://`, a następnie nazwą obrazu. Zobacz sekcje "runs" i "runs.image" w [dokumentacji](https://docs.github.com/en/actions/reference/workflows-and-actions/metadata-syntax#runsimage) dla dodatkowych informacji.
- [ ] `README.md`
> Chociaż plik `README.md` jest zalecany przez GitHub dla działań publikowanych w Marketplace, nie jest on wymagany.
- [ ] `.dockerignore`
- [ ] `CONTRIBUTING.md`
