---
question: "As ações de JavaScript e `actions/github-script` ambas utilizam JavaScript. Por que você deveria usar `actions/github-script` em vez de criar sua própria ação em JavaScript?"
documentation: "https://github.com/actions/github-script"
---

- [x] `actions/github-script` deve ser usado para scripts curtos embutidos
- [x] `actions/github-script` deve ser usado quando você quiser usar um cliente pré-autenticado para interagir com a API do GitHub.
- [x] Ações de JavaScript devem ser usadas quando você quiser uma ação personalizada reutilizável para ser utilizada em vários repositórios
- [ ] Ações de JavaScript devem ser usadas para scripts curtos embutidos
- [ ] `actions/github-script` deve ser usado quando você precisar utilizar um ambiente Node.js ajustado com várias dependências específicas
> Embora seja possível instalar módulos para usar no `actions/github-script` antes de chamá-lo, se várias dependências forem necessárias, isso resultará em várias etapas no fluxo de trabalho. `actions/github-script` também não permite alterar a versão do Node.js; você está limitado à versão definida por ele.
- [ ] Ações de JavaScript devem ser usadas quando você quiser uma solução de baixo custo para fazer chamadas à API do GitHub.
> Ações de JavaScript não têm baixo custo; elas exigem a criação de um arquivo `action.yml`, que por sua vez deve ser armazenado em sua própria pasta ou até mesmo em seu próprio repositório, dependendo da abordagem. `actions/github-script` vem com um cliente pré-autenticado que facilita fazer chamadas à API do GitHub usando uma abordagem baseada em JavaScript.
