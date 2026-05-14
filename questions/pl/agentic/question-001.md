---
question: "W niestandardowym profilu agenta dla GitHub Copilot, który klucz YAML na najwyższym poziomie jest używany do deklarowania serwerów MCP, do których agent może uzyskać dostęp?"
documentation: "https://docs.github.com/en/copilot/reference/custom-agents-configuration"
---

- [x] `mcp-servers`
> Klucz `mcp-servers` definiuje konfiguracje serwerów MCP, w tym typ, polecenie, argumenty, narzędzia i zmienne środowiskowe.
- [ ] `tools`
> `tools` wymienia, z jakich narzędzi agent może korzystać, ale nie definiuje konfiguracji serwerów MCP.
- [ ] `servers`
> W schemacie YAML niestandardowego profilu agenta nie ma klucza `servers`.
- [ ] `extensions`
> `extensions` nie jest prawidłowym kluczem w frontmatterze profilu agenta.
