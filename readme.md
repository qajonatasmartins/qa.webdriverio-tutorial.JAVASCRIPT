# qa.webdriverio-tutorial.JAVASCRIPT

Projeto de automação de testes passo a passo.

A branch `main` se refere-se a aula 01 do video [Como criar um projeto de automação de testes web com WebdriverIO](https://www.youtube.com/watch?v=W8iMxo_zeyY&list=PLFr5ujjslsZNXbv6aktQ7acrNMskCRRXm&ab_channel=QAJonatasMartins)

As demais branchs do projeto contém cada aula ministrada no youtube.

Veja as demais branchs do projeto com as evoluções do projeto de testes com webdriverio.

Me siga nas redes sociais 🫶🏻🐞

<p align="center">
	<a href="https://github.com/jonatasmfaria"><img alt="github" width="10%" style="padding:5px" src="https://img.icons8.com/clouds/100/000000/github.png"/></a>
	<a href="https://www.linkedin.com/in/jonatasmfaria/"><img alt="linkedin" width="10%" style="padding:5px" src="https://img.icons8.com/clouds/100/000000/linkedin.png"/></a>
	<a href="https://www.youtube.com/channel/UCD2fgVj5Yt8roBtWHXDLykg"><img alt="youtube" width="10%" style="padding:5px" src="https://img.icons8.com/clouds/344/youtube.png"/></a>
	<a href="https://www.instagram.com/qajonatasmartins/"><img alt="instagram" width="10%" style="padding:5px" src="https://img.icons8.com/clouds/100/000000/instagram.png"/></a>
</p>

## Pre-requisitos para rodar o projeto

- Node Js
- Navegador Chrome

## Para instalar o projeto

Execute o comando `npm install`

## Para rodar os testes

Execute `npm run wdio`

## IMPORTANTE

A pasta `test` gerada pelo webdriverio foi renomeada para `tests`

## Erros e solçuões

1. Erro `pattern ./test/specs/**/*.js did not match any file` ao executar os testes do webdriverio

**Problema**

O erro abaixo foi apresentado porque o nome da pasta `tests` estava incorreto no arquivo de configuração(wdio.conf.js) do webdriverio.

 WebdriverIO git:(aula-02) ✗ npm run wdio

webdriverio-tests@0.1.0 wdio
wdio run wdio.conf.js

2022-10-04T23:20:01.708Z WARN @wdio/config:ConfigParser: pattern ./test/specs/**/*.js did not match any file

Execution of 0 workers started at 2022-10-04T23:20:01.715Z

2022-10-04T23:20:01.740Z INFO @wdio/cli:launcher: Run onPrepare hook
2022-10-04T23:20:01.741Z INFO chromedriver: Start Chromedriver (/Users/jonatasmartins/Documents/Projetos/qajonatasmartins/WebdriverIO/node_modules/chromedriver/lib/chromedriver/chromedriver) with args --port=9515 --url-base=/
2022-10-04T23:20:01.766Z INFO chromedriver: Starting ChromeDriver 105.0.5195.52 (412c95e518836d8a7d97250d62b29c2ae6a26a85-refs/branch-heads/5195@{#853}) on port 9515
2022-10-04T23:20:01.766Z INFO chromedriver: Only local connections are allowed.
2022-10-04T23:20:01.766Z INFO chromedriver: Please see https://chromedriver.chromium.org/security-considerations for suggestions on keeping ChromeDriver safe.
2022-10-04T23:20:01.778Z INFO chromedriver: ChromeDriver was started successfully.
2022-10-04T23:20:01.853Z WARN @wdio/config:ConfigParser: pattern ./test/specs/**/*.js did not match any file
2022-10-04T23:20:01.853Z ERROR @wdio/cli:launcher: No specs found to run, exiting with failure
2022-10-04T23:20:01.854Z INFO @wdio/cli:launcher: Run onComplete hook

**Solução**

- Abra o arquivo wdio.conf.js
- Pesquise por `specs:` e altere a string com o nome da pasta `test` para `tests`.

Antes:
```
    specs: [
        './test/specs/**/*.js'
    ],
```
Depois:
```
    specs: [
        './tests/specs/**/*.js'
    ],
```

2. 