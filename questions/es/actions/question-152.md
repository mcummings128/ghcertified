---
question: "Complete el espacio en blanco: Al usar runners autohospedados, la caché de herramientas ___"
documentation: "https://docs.github.com/en/enterprise-server/admin/managing-github-actions-for-your-enterprise/managing-access-to-actions-from-githubcom/setting-up-the-tool-cache-on-self-hosted-runners-without-internet-access"
---

- [x] comienza vacía y debe llenarse para guardar herramientas entre ejecuciones
> Las cachés de herramientas permiten almacenar diferentes versiones de herramientas, lo que facilita una actividad más rápida de los runners autohospedados. Sin cachés de herramientas, los runners autohospedados que usan `actions/setup-*` tardarán más en ejecutarse.
- [ ] comienza igual que los runners hospedados por GitHub, ya que viene prellenada con ciertas herramientas
> Aunque los runners hospedados por GitHub sí vienen con ciertas herramientas preinstaladas, este no es el caso de los runners autohospedados.
- [ ] comienza con las mismas herramientas que los runners hospedados por GitHub, así como con una selección de herramientas personalizadas para mejorar la gestión de los runners autohospedados
- [ ] no puede ser llenada

