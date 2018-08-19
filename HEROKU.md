> [Home](README.md)

#### Heroku:

* Baixar o **Heroku CLI** (Command Line Interface) no site da [*Heroku*](https://www.heroku.com).

##### Comandos:

* `heroku version`;
* `heroku login`;
* `heroku keys` para verificar as chaves *SSH* cadastradas;
* `heroku create [APP]` para criar o projeto chamado *APP*;
* `heroku apps` para listar os projetos;
* `heroku apps:rename --app [NOME_ANTIGO] [NOME_NOVO]` para renomear o projeto *NOME_ANTIGO* para *NOME_NOVO*;
* `heroku open` para abrir o browser na página inicial do sistema;
* `heroku logs --tail` para exibir os logs;
* `heroku run java --app=[NOME_PROJETO] -version` para verificar a versão do *Java* no projeto de nome *NOME_PROJETO*;
* `heroku apps:destroy --app=[NOME_PROJETO] --confirm [NOME_PROJETO]` para excluir o projeto de nome *NOME_PROJETO*;
* `heroku info` para verificar os dados do projeto;
* `heroku config` para exibir o valor das variáveis de configuração;
* `heroku maintenance:on` para iniciar o modo de manutenção do sistema no heroku. Para desativar é só trocar o **:on** por **:off**. [Heroku | Maintenance Mode](https://devcenter.heroku.com/articles/maintenance-mode);
  * Pode se customizar a página de manutenção com o seguinte comando: `heroku config:set MAINTENANCE_PAGE_URL=//s3.amazonaws.com/<your_bucket>/your_maintenance_page.html`.

##### Angular:

* Após finalizada a escrita do código do app *Angular*, podemos preparar as configurações para o deploy no **Heroku**:
  * Precisamos instalar o *Angular CLI* na aplicação para que o *Heroku* possa utiliza-lo: `npm install @angular/cli @angular/compiler-cli --save`;
  * Alterar o arquivo `package.json`, fazendo as seguintes alterações:
    * Adicionar pela propriedade "scripts" a seguinte entrada: `"postinstall": "ng build --output-path dist"`;
	* Mover as entradas `@angular/cli` e `@angular/compiler-cli` da propriedade `"devDependencies"` para a propriedade `"dependencies"`.
  * Após feita as alterações no arquivo `package.json` é necessário fazer o **push** para o *remote* do *heroku* com o comando `git push heroku master`.
  * Use o comando `heroku open` para abrir o navegador com aplicação.
  * [Dúvidas](https://devcenter.heroku.com/articles/mean-apps-restful-api).

> [Home](README.md)