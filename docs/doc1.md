---
id: doc1
title: Documentação
sidebar_label: Example Page
---

## Pré-requisitos

- Node.js
- Docusaurus

`yarn add global docusaurus-init` ou `npx docusaurus-init` ou `npm install docusaurus-init`

## Criar o projeto

No terminal:

-- Criar e acessar pasta

> mkdir `<nome-do-projeto>`

> cd `<nome-do-projeto>`

## Gerar build

Configure o arquivo siteConfig:

`url: 'https://USERNAME.github.io',`
`baseUrl: '/nome-do-projeto/',`
`projectName: 'nome-do-projeto',` _\*opcional_

Na pasta raiz digite:

> cd website

> yarn build

## Iniciar repositório

> git init

- Adicionar o repositório remoto
  > git remote add origin `git@github.com:username/<nome-do-projeto>.git`

> git add .

> git commit -m "first commit"

> git push origin master

## Publicar o site estático no GitHub Pages

Para isso será necessário criar uma branch com os arquivos do diretório website/build/\<nome-do-projeto>.
Na pasta raiz digite:

> git checkout -b \<nome-da-branch>

> git add -f website/build/\<nome-do-projeto>.

o parâmetro **-f** serve para forçar o track do diretório website/build, já que por default o arquivo .ignore está configurado para não rastreá-lo.

> git commit -m "initial dist subtree"

> git subtree push --prefix website/build/\<nome-do-projeto> origin \<nome-da-branch>

Pronto! O site já está em funcionamento!

```
<script src="mermaid.js"></script>

<script>
    mermaid.mermaidAPI.initialize({
        startOnLoad:false
    });
    $(function(){
        // Example of using the API
        var element = document.querySelector("#graphDiv");

        var insertSvg = function(svgCode, bindFunctions){
            element.innerHTML = svgCode;
        };

        var graphDefinition = 'graph TB\na-->b';
        var graph = mermaid.mermaidAPI.render('graphDiv', graphDefinition, insertSvg);
    });
</script>

```
