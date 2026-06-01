---
question: "Mercedes quer publicar uma ação de contêiner Docker que ela criou no GitHub Actions Marketplace. Quais arquivos ela precisa, no mínimo, para fazer isso?"
documentation: "https://docs.github.com/en/actions/how-tos/create-and-publish-actions/publish-in-github-marketplace"
---

- [x] `action.yml`
> Um arquivo `action.yml` é necessário para que uma ação seja publicada no Marketplace, independentemente do tipo.
- [x] Um `Dockerfile`, se a imagem for construída como parte da ação durante a execução do workflow
> Ações de contêiner Docker só exigem um `Dockerfile` se a imagem precisar ser criada do zero e não puder ser obtida de um registro de imagens. O valor de `runs.image` em `action.yml` deve ser o caminho para o `Dockerfile`.
- [ ] Um `Dockerfile`, se a imagem for referenciada de um registro de imagens
> Ao referenciar uma imagem em um registro de imagens, nenhum `Dockerfile` é necessário. O valor da chave `runs.image` em `action.yml` deve ter o prefixo `docker://` seguido pelo nome da imagem. Consulte as seções "runs" e "runs.image" na [documentação](https://docs.github.com/en/actions/reference/workflows-and-actions/metadata-syntax#runsimage) para mais informações.
- [ ] `README.md`
> Embora um arquivo `README.md` seja recomendado pelo GitHub para Ações publicadas no Marketplace, não é um requisito obrigatório.
- [ ] `.dockerignore`
- [ ] `CONTRIBUTING.md`
