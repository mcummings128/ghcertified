---
question: "En un perfil de agente personalizado para GitHub Copilot, ¿qué clave de nivel superior en el frontmatter YAML se utiliza para declarar los servidores MCP a los que el agente puede acceder?"
documentation: "https://docs.github.com/en/copilot/reference/custom-agents-configuration"
---

- [x] `mcp-servers`
> La clave `mcp-servers` define configuraciones del servidor MCP, incluyendo tipo, comando, argumentos, herramientas y variables de entorno.
- [ ] `tools`
> `tools` enumera las herramientas que el agente puede usar, pero no define configuraciones del servidor MCP por sí mismo.
- [ ] `servers`
> No existe una clave `servers` en el esquema YAML del agente personalizado.
- [ ] `extensions`
> `extensions` no es una clave válida en el frontmatter del perfil del agente personalizado.
