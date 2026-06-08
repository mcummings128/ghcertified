---
question: "Uma organização possui vários repositórios que compartilham um ambiente especializado de Node.js hospedado em uma rede privada. O próximo objetivo da organização envolve a configuração de um software de bloqueio de nós dentro dessa rede. Qual das opções a seguir atenderia melhor às necessidades da organização ao executar workflows?"
documentation: "https://docs.github.com/en/actions/concepts/runners/self-hosted-runners"
---

- [x] Runners auto-hospedados configurados no nível da organização
- [ ] Um runner auto-hospedado por repositório, configurado no nível do repositório
> Isso seria duplicado e complexo de gerenciar. Os repositórios podem referenciar o mesmo runner no nível da organização, que é a abordagem correta nesta situação.
- [ ] Runners hospedados no GitHub, com todos os workflows utilizando `actions/setup-node`
> Os runners hospedados no GitHub são [efêmeros](https://docs.github.com/en/actions/concepts/runners/github-hosted-runners#overview-of-github-hosted-runners), o que significa que uma nova instância do runner é configurada para cada execução de workflow. Isso não funcionaria bem com um software de bloqueio de nós, que só permite que o software seja executado em um dispositivo/VM específico. Além disso, embora os runners hospedados no GitHub possam ser configurados para acessar redes privadas, isso não é uma funcionalidade pronta para uso.
- [ ] Runners hospedados no GitHub configurados no nível da organização
> Runners hospedados no GitHub não podem ser configurados desta forma.
- [ ] Runners hospedados no GitHub, utilizando `runs-on: [node<version>]` (`<versão>` sendo a versão desejada do Node) em todos os workflows.
> `[node<version>]` não aponta para nenhum runner hospedado no GitHub.
