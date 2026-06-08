---
question: "A organização de Ingrid possui um subconjunto de runners Linux auto-hospedados que devem ser usados apenas por determinados repositórios. Qual é a melhor abordagem para ela impor esse comportamento?"
documentation: "https://docs.github.com/en/actions/how-tos/manage-runners/self-hosted-runners/manage-access#changing-which-repositories-can-access-a-runner-group"
---

- [x] Crie um novo grupo de runners, adicione os runners ao grupo e selecione quais repositórios têm acesso permitido ao grupo nas configurações do grupo.
- [ ] Crie um novo label de runner, adicione os labels aos runners e selecione quais repositórios têm acesso permitido ao label nas configurações do label.
- [ ] Crie um novo label de runner, adicione os labels aos runners e certifique-se de que todos os workflows nos repositórios incluam esse label no campo `runs-on` de seus arquivos.
> Labels não limitam o acesso aos runners. Apenas adicionar um label não funcionará; adicionar labels ao `runs-on` pode potencialmente afetar o fluxo de trabalho correspondente, impedindo que encontre um runner para executar.
- [ ] Crie um novo grupo de runners, selecione "Linux" como o sistema operacional e use padrões glob para definir quais repositórios têm acesso permitido nas configurações do grupo.  
