# cdn
Automação de testes mobile utilizando o aplicativo da CDN (capivara).

Essa automação de testes foi construída com base na documentação do framework maestro: https://maestro.mobile.dev/ utilizando o padrão de projeto page objects.
Os elementos de interface são identificados em arquivos XX.js, proporcionando maior clareza na escrita do código, pensando em manutenção de ID's no futuro.
O fluxo de login com o caso de teste positivo onde são feitas validaçóes na tela esta na pasta login com o nome loginCapivara.yaml. Existe outro fluxo que se chama perfilCapivara onde o mesmo chama o fluxo de login e os interliga, possibilidade que pode ser adicionada a outros fluxos do app no futuro.

Foi feita a construção parelela de um arquivo chamado "manual.yml" dentro da pasta workflows do github onde é utilizada uma imagem com as configurações necessárias para executar o teste dentro de uma pipeline de testes automatizados.
Também foi feita uma opção utilizando o maestro cloud onde se pode paralelizar a execução e também obter videos da execução do teste na branch develop. 

O arquivo .apk foi incluido no repositorio para a utilização do mesmo na imagem em docker criada. Para a execução no maestro cloud o arquivo fica na nuvem.


Como executar localmente:

- Para executar localmente você precisa configurar sua máquina dependendo do seu sistema operacional. Para esse projeto eu utilizei um notebook pessoal windows.
As instruções estão nessa pagina: https://maestro.mobile.dev/getting-started/installing-maestro

- Após essa configuração e instalação você pode executar o comando maestro test loginCapivara.yaml dentro da pasta do projeto e com o emulador aberto, provendo o adb necessário para os testes. No proprio console você consegue visualizar os resultados dos testes, porém
se executar maestro test maestro/android/login/loginCapivara.yaml --format=junit --output=report.xml --no-ansi terás um report em xml. Você pode trocar os parametros para html também, caso queira o report em html.

Alguns videos com execuções de demonstração:

O video 3 mostra a interface do maestro cloud que esta na branch develop com outro github action.

https://drive.google.com/drive/folders/1f2CkoRhU2HtcUR83vRZvXcxAlIK2JcBF?usp=sharing
