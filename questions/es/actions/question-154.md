---
question: "¿Cuándo construirías una acción de contenedor Docker para compartir en el marketplace de GitHub Actions?"
documentation: "https://docs.github.com/en/actions/concepts/workflows-and-actions/custom-actions#docker-container-actions"
---

- [x] Las acciones de contenedor Docker garantizan un entorno de ejecución consistente y dependencias específicas sin que los usuarios necesiten manejar estos aspectos por sí mismos
- [ ] Las acciones de contenedor Docker son una acción de bajo costo y lista para usar
> Las acciones de contenedor Docker no se consideran de bajo costo, ya que requieren el uso de una imagen (preconstruida o especificada mediante el archivo `Dockerfile`), un script de punto de entrada y, posiblemente, lógica previa y posterior al punto de entrada.
- [ ] Las acciones de contenedor Docker tienen un inicio rápido en runners de Windows y macOS
> Los contenedores Docker solo pueden ejecutarse en runners con sistema operativo Linux (`ubuntu-latest` para los runners alojados por GitHub). También tardan más en comparación con las acciones JavaScript y compuestas.
- [ ] Las acciones de contenedor Docker son un conjunto de pasos dentro de otros flujos de trabajo que se ejecutan en el contexto del flujo/acción que los llama
> Un "conjunto reutilizable de pasos" describe una acción compuesta, no una acción de contenedor Docker.
- [ ] Las acciones de contenedor Docker te permiten utilizar Docker sin requerir un archivo `action.yml`
> Todas las acciones, independientemente del tipo, deben usar un archivo `action.yml`
