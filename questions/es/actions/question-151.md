---
question: "¿Qué deberías usar al pasar información entre trabajos: salidas de trabajo o `GITHUB_ENV`?"
documentation: "https://docs.github.com/en/actions/how-tos/write-workflows/choose-what-workflows-do/use-variables#passing-values-between-steps-and-jobs-in-a-workflow"
---

- [x] Salidas de trabajo, porque el valor de las variables ambientales establecidas escribiendo en `GITHUB_ENV` solo se aplica al trabajo actual.
> Aunque `env` puede configurarse a nivel de flujo de trabajo (lo que significa que sus variables pueden ser referenciadas por múltiples trabajos), esto no significa que cambiar el valor de la variable ambiental persista más allá del trabajo que la cambió.
- [ ] `GITHUB_ENV`, porque las salidas de trabajo solo pueden establecerse y referenciarse dentro del mismo trabajo.
- [ ] Salidas de trabajo, porque son más fáciles de configurar.
> Configurar y referenciar las salidas de trabajo es más complicado que utilizar `GITHUB_ENV`. Por ejemplo, las salidas de trabajo requieren configurar un bloque `outputs`, agregar un `id` a un paso y usar `needs` para indicar dependencias.
- [ ] `GITHUB_ENV`, porque usarlo para establecer variables ambientales reduce significativamente la carga en el runner, disminuyendo el tiempo de ejecución del flujo de trabajo.
