---
question: "Mercedes quiere publicar una acción de contenedor Docker que ha creado en el GitHub Actions Marketplace. ¿Qué archivos necesita como mínimo para hacerlo?"
documentation: "https://docs.github.com/en/actions/how-tos/create-and-publish-actions/publish-in-github-marketplace"
---

- [x] `action.yml`
> Un archivo `action.yml` es necesario para que una acción sea publicada en el Marketplace, independientemente del tipo.
- [x] Un `Dockerfile`, si la imagen se crea como parte de la acción durante la ejecución del workflow
> Las acciones de contenedor Docker solo requieren un `Dockerfile` si la imagen debe ser creada desde cero y no puede ser extraída de un registro de imágenes. El valor de `runs.image` en `action.yml` debe ser la ruta hacia el `Dockerfile`.
- [ ] Un `Dockerfile`, si la imagen se va a referenciar desde un registro de imágenes
> Cuando se hace referencia a una imagen en un registro de imágenes, no se necesita un `Dockerfile`. El valor de la clave `runs.image` en `action.yml` debe estar precedido por `docker://` seguido del nombre de la imagen. Consulta las secciones "runs" y "runs.image" en la [documentación](https://docs.github.com/en/actions/reference/workflows-and-actions/metadata-syntax#runsimage) para más información.
- [ ] `README.md`
> Aunque GitHub recomienda incluir un archivo `README.md` para las acciones que se publican en el Marketplace, no es un requisito estricto.
- [ ] `.dockerignore`
- [ ] `CONTRIBUTING.md`
