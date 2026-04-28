---
question: "O que a configuração padrão de análise CodeQL no GitHub faz?"
documentation: "https://docs.github.com/en/code-security/code-scanning/introduction-to-code-scanning/about-code-scanning-with-codeql#about-code-scanning-with-codeql"
---

- [x] Detecta automaticamente as linguagens, seleciona o conjunto de consultas padrão e configura os gatilhos de análise
- [ ] Exige que os usuários selecionem linguagens e definam um conjunto de consultas personalizado antes que as análises possam ser executadas
> Uma caixa de diálogo de confirmação é exibida ao habilitar a configuração padrão, mas as linguagens e o conjunto de consultas são automaticamente pré-selecionados
- [ ] Analisa apenas a linguagem principal do repositório usando o conjunto de consultas estendido
> A configuração padrão analisa todas as linguagens suportadas, não apenas a principal, e utiliza o conjunto de consultas padrão
- [ ] Cria um arquivo de workflow CodeQL no repositório que deve ser mesclado antes do início da análise
> Isso descreve a configuração avançada, não a configuração padrão
