---
question: "Quais das seguintes afirmações são verdadeiras sobre chamar workflows reutilizáveis em comparação com chamar ações compostas?"
documentation: "https://docs.github.com/en/actions/concepts/workflows-and-actions/reusing-workflow-configurations#key-differences-between-reusable-workflows-and-composite-actions"
---

- [x] Ações compostas são chamadas através da referência à pasta que contém seu arquivo `action.yml`.
> Como uma ação, ações compostas devem conter a maior parte de sua lógica dentro de um arquivo `action.yml`. Para chamar a ação composta, basta apontar para onde seu arquivo `action.yml` está localizado (isso inclui o diretório raiz. Ex.: para chamar uma ação composta que está localizada no diretório raiz do mesmo repositório que o workflow chamador, a sintaxe `uses: ./` seria usada).
- [ ] Workflows reutilizáveis são chamados através da referência à pasta que contém seu arquivo `action.yml`.
> Workflows reutilizáveis são arquivos regulares `.yml` ou `.yaml` que estão armazenados em `.github/workflows`. Eles não possuem um arquivo `action.yml`.
- [x] Ações compostas devem ser chamadas como um passo dentro de um trabalho (job).
> Ações compostas (assim como qualquer outra ação) são chamadas de dentro de um passo de um trabalho do workflow — em outras palavras, não é necessário um trabalho específico do workflow apenas para chamar uma ação composta.
- [x] Workflows reutilizáveis devem ser chamados no nível de trabalho do workflow (não no nível de passo).
> Passos dentro de um trabalho do workflow não podem chamar um workflow reutilizável. Um workflow reutilizável deve ser chamado por um trabalho individual dentro do workflow chamador. Isso pode resultar em um ou mais trabalhos sendo executados no workflow chamador (esses trabalhos podem ser vistos nas execuções do workflow na interface do usuário do GitHub Actions).
- [ ] Segredos podem ser passados tanto para workflows reutilizáveis quanto para ações compostas que estão sendo chamadas através do bloco `uses.secrets`.
> Apenas workflows reutilizáveis podem ser chamados usando o bloco `secrets`. Para passar segredos para uma ação composta, é necessário usar soluções alternativas (como passar o segredo como uma entrada).
- [ ] Apenas workflows reutilizáveis podem aceitar entradas.
> Tanto workflows reutilizáveis quanto ações compostas podem aceitar entradas.
- [x] Workflows reutilizáveis podem usar um tipo de runner diferente do workflow chamador, enquanto ações compostas não podem.
> Workflows reutilizáveis possuem jobs como qualquer outro workflow, e esses jobs podem especificar diferentes tipos de runner através da chave `jobs.runs-on`. Ações compostas herdam o ambiente do runner do trabalho do workflow chamador.
