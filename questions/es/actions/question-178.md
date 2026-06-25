---
question: "Debes asegurarte de que tu entorno `prod` requiera aprobaciones manuales antes de que los despliegues puedan proceder. De las siguientes opciones, ¿cuáles son verdaderas con respecto a cómo se configura esto?"
documentation: "https://docs.github.com/en/actions/reference/workflows-and-actions/deployments-and-environments#required-reviewers"
---

- [x] Si enumeras revisores requeridos, solo uno de ellos necesita aprobar para continuar con el despliegue.
- [x] Puedes prevenir auto-revisiones en caso de que la persona que quiera desplegar también sea un revisor requerido.
- [ ] Si enumeras revisores requeridos, todos ellos necesitan aprobar para continuar con el despliegue.
> Sorprendentemente, solo uno de los revisores requeridos necesita aprobar el trabajo del flujo de trabajo. Para hacer cumplir este comportamiento, deberías crear una regla de protección de despliegues personalizada a través de una aplicación de GitHub.
- [ ] No puedes prevenir auto-revisiones, pero puedes configurar alertas para ver quién activó el despliegue.
- [ ] Solo los usuarios individuales pueden ser asignados como revisores requeridos, no los equipos.
> Tanto los usuarios individuales como los equipos pueden ser asignados como revisores requeridos.
- [ ] Los revisores requeridos necesitan al menos acceso de `write` al repositorio para aprobar.
> Los revisores requeridos necesitan al menos acceso de `read`.
