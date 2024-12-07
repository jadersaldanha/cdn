# cdn
Automação de testes mobile utilizando o aplicativo da CDN (capivara).

Essa automação de testes foi construída com base na documentação do framework maestro: https://maestro.mobile.dev/ utilizando o padrão de projeto page objects.
Os elementos de interface são identificados no arquivo login.js, proporcionando maior clareza na escrita do código, pensando em manutenção de ID's no futuro.
O fluxo de login com o caso de teste positivo onde são feitas validaçóes na tela esta na pasta login com o nome loginCapivara.yaml.

Foi feita a construção parelela de um arquivo chamado "manual.yml" dentro da pasta workflows do github onde é utilizada uma imagem com as confirações necessárias para executar o teste dentro de uma pipeline de testes automatizados.
Também foi feita uma opção utilizando o maestro cloud onde se pode paralelizar a execução e também obter videos da execução do teste. 

O arquivo .apk foi incluido no repositorio para a utilização do mesmo na imagem em docker criada. 


Como executar localmente:

- Para executar localmente você precisa configurar sua máquina dependendo do seu sistema operacional. Para esse projeto eu utilizei um notebook pessoal windows.
As instruções estão nessa pagina: https://maestro.mobile.dev/getting-started/installing-maestro

- Após essa configuração e instalação você pode executar o comando maestro test loginCapivara.yaml dentro da pasta do projeto e com o emulador aberto, provendo o adb necessário para os testes.

