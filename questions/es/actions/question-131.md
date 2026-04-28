---
question: "¿Cuál de las siguientes afirmaciones son correctas respecto a la llamada a workflows reutilizables frente a la llamada a acciones compuestas?"
documentation: "https://docs.github.com/en/actions/concepts/workflows-and-actions/reusing-workflow-configurations#key-differences-between-reusable-workflows-and-composite-actions"
---

- [x] Las acciones compuestas se llaman haciendo referencia a la carpeta que contiene su archivo `action.yml`.
> Como acción, las acciones compuestas deben contener la mayor parte de su lógica dentro de un archivo `action.yml`. Para llamar a la acción compuesta, apunta al lugar donde se encuentra su `action.yml` (incluyendo la raíz. Por ejemplo, para llamar a una acción compuesta que se encuentra en la raíz del mismo repositorio que el workflow que la llama, se utilizaría la sintaxis `uses: ./`).
- [ ] Los workflows reutilizables se llaman haciendo referencia a la carpeta que contiene su archivo `action.yml`.
> Los workflows reutilizables son archivos regulares `.yml` o `.yaml` que se almacenan en `.github/workflows`. No tienen un archivo `action.yml`.
- [x] Las acciones compuestas deben ser llamadas como un paso dentro de un job.
> Las acciones compuestas (al igual que cualquier otra acción) se llaman dentro de un paso de un job de workflow. En otras palabras, no necesitas un job específico del workflow solo para llamar a una acción compuesta.
- [x] Los workflows reutilizables deben ser llamados a nivel de job del workflow (no desde el nivel de paso).
> Los pasos dentro de un job de workflow no pueden llamar a un workflow reutilizable. Un workflow reutilizable debe ser llamado por un job individual dentro del workflow que lo llama. Esto puede resultar en uno o más jobs ejecutándose en el workflow que realiza la llamada (dichos jobs se pueden ver en las ejecuciones de workflows en la interfaz de usuario de GitHub Actions).
- [ ] Los secretos se pueden pasar tanto a workflows reutilizables como a acciones compuestas mediante el bloque `uses.secrets`.
> Solo los workflows reutilizables pueden ser llamados utilizando el bloque `secrets`. Para pasar secretos a una acción compuesta, deben usarse soluciones alternativas (como pasar el secreto como entrada).
- [ ] Solo los workflows reutilizables pueden aceptar entradas.
> Tanto los workflows reutilizables como las acciones compuestas pueden aceptar entradas.
- [x] Los workflows reutilizables pueden usar un tipo de runner diferente al del workflow que los llama, mientras que las acciones compuestas no pueden.
> Los workflows reutilizables tienen jobs como cualquier otro workflow, y esos jobs pueden especificar un tipo de runner diferente mediante la clave `jobs.runs-on`. Las acciones compuestas heredan el entorno del runner del job del workflow que las llama.
