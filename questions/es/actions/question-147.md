---
question: "Tienes un secreto codificado en base-64 que decodificas en un flujo de trabajo de GitHub Actions. ¿Cómo puedes asegurarte de que el secreto decodificado no aparezca accidentalmente en el registro del flujo de trabajo?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/workflow-commands#masking-a-value-in-a-log"
---

- [x] Usando el comando de flujo de trabajo `add-mask` en los trabajos donde se pueda utilizar el secreto decodificado.
> Usar `add-mask` enmascarará valores que GitHub Actions no detecta como un secreto. Esto debe hacerse una vez por valor, por cada trabajo que utilice el secreto decodificado.
- [ ] No es necesario hacer nada, ya que la infraestructura de GitHub Actions redacta automáticamente los secretos decodificados.
> No está garantizado que GitHub Actions pueda detectar automáticamente y redactar secretos transformados según la [documentación](https://docs.github.com/en/actions/reference/security/secure-use#use-secrets-for-sensitive-information).  
- [ ] Evitar el uso de declaraciones print que contengan el secreto decodificado, ya que esta es la única manera en que el secreto decodificado podría aparecer en el registro del flujo de trabajo.
> Aunque se recomienda evitar las declaraciones print que contengan secretos decodificados, los secretos decodificados pueden aparecer en otros lugares del registro del flujo de trabajo, como en mensajes relacionados con llamadas a la API.
- [ ] Usar la función integrada `maskSecret` para enmascarar el secreto decodificado en las instancias donde pueda ser utilizado.
> `maskSecret` no es una función integrada proporcionada por GitHub Actions.
