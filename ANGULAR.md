> [Home](README.md)

#### Angular:

##### Para trabalhar com o Angular vamos precisar:

* Uma *IDE* compatível com [TypeScript](https://www.typescriptlang.org/). Ex.: [Visual Studio Code](https://code.visualstudio.com/);
* [Node.js](https://nodejs.org/en/). O *Node.js* é necessário para se usar em tempo de desenvolvimento, pois em produção o usuário utilizará o browser para acessar a aplicação;
  - Para instalar no [linux](NODE_LINUX.md);
  - Para verificar se o *Node* foi instalado é só usar o seguinte comando no terminal: `node -v`.
* [npm](https://www.npmjs.com/). O *npm* é instalado junto com o *node.js*. O *npm* é um gerenciador de pacotes que permiti instalar bibliotecas e ferramentas em nossos projetos;
  - Para verificar se o *npm* foi instalado é só usar o seguinte comando no terminal: `npm -v`.
* [Angular CLI](https://cli.angular.io/). Ferramenta de linha de comando para ajudar a criar aplicações *Angular* seguindo as melhores práticas;
  - Para instalar usar o seguinte comando no terminal: `npm install -g @angular/cli`;
    - -g = global
  - Para verificar se o *npm* está instalado: `ng -v`;
  - Para criar um novo projeto: `ng new [NOME_PROJETO]`; 
  - Para gerar novos componentes: `ng g c [NOME_COMPONENTE] --spec=false`;
    - `--spec=false` serve para não gerar os arquivos de teste.
  - Para inicia um servidor de testes: `ng serve`. 

> [Home](README.md)