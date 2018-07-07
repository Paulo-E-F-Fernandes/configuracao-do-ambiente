# Configuração do Ambiente

### Este projeto foi criado para server como um guia para a configuração de ambiente e também para ferrametas úteis que acabamos esquecendo.

#### [Versionamento:](VERSIONAMENTO.md)

* [Git](https://git-scm.com/);
* Para gerar a chave ssh podemos usar os seguintes passos:
  - https://help.github.com/enterprise/2.13/user/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/#platform-windows;
* [GitKraken](https://www.gitkraken.com/) - GUI para o Git;
* **OBS.:**
  - Caso ocorrer algum problema parecido com o abaixo:
    ```
    $ git pull origin master
    ssh: connect to host bitbucket.org port 22: Network is unreachable
    fatal: Could not read from remote repository.

    Please make sure you have the correct access rights
    and the repository exists.
    ```
  - Podemos resolver usando o seguinte:
    - Abrir um console do *Git Bash*;
    - Digitar `nano  ~/.ssh/config`;
    - E depois:
      ```
      Host bitbucket.org
        Hostname altssh.bitbucket.org
        Port 443
      ```
