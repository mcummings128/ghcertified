---
question: "Dorothea está solucionando problemas de un flujo de trabajo activado por un evento de push y está interesada en ver detalles sobre el webhook. ¿Cómo puede ver todo el payload del webhook que activó el flujo de trabajo?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/contexts#github-context"
---

- [x] Imprimiendo el contenido del objeto `github.event` en un paso
> `github.event` mostrará el payload completo del webhook del evento. Este payload varía según el tipo de evento. Consulta [Webhook events and payloads](https://docs.github.com/en/webhooks/webhook-events-and-payloads) para más detalles.
- [ ] Marcando la casilla "Show event webhook payload" en las opciones de ejecución del flujo de trabajo.
- [ ] Configurando un secreto o variable llamada `SHOW_EVENT_PAYLOAD` en `true`
- [ ] Navegando a la sección "Webhooks" en la configuración del repositorio
> La sección "Webhooks" en la configuración del repositorio solo mostrará detalles de los webhooks personalizados, no de los webhooks estándar de eventos como `push`.
