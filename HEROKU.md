> [Home](README.md)

#### Heroku:

##### Angular:

* Após finalizada a escrita do código do app *Angular*, podemos preparar as configurações para o deploy da aplicação no **Heroku**:
  * Precisamos instalar o *Angular CLI* na aplicação para que o *Heroku* possa utiliza-lo: `npm install @angular/cli @angular/compiler-cli --save`;
  * Alterar o arquivo `package.json`, fazendo as seguintes alterações:
    * Adicionar pela propriedade "scripts" a seguinte entrada: `"postinstall": "ng build --output-path dist"`;
	* Mover as entradas `@angular/cli` e `@angular/compiler-cli` da propriedade `"devDependencies"` para a propriedade `"dependencies"`.
  * Após feita as alterações no arquivo `package.json` é necessário fazer o **push** para o *remote* do *heroku* com o comando `git push heroku master`.
  * Use o comando `heroku open` para abrir o navegador com aplicação.

> [Home](README.md)