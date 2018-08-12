> [Home](README.md)

#### Versionamento:

* [Git](https://git-scm.com/);
* Para gerar a chave ssh podemos usar os seguintes passos:
  - https://help.github.com/enterprise/2.13/user/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/#platform-windows;
* [GitKraken](https://www.gitkraken.com/) - GUI para o Git;
* Após a criação do repositório remoto no `GitHub`, `BitBucket` ou qualquer outro repositório remoto, é necessário criar o repositório local e adicionar o endereço para o repositório remoto;
  - Entrar no diretório do projeto e executar os comandos:
    - `git init` - Para iniciar o repositório git local;
	- `git remote add [NOME_REPOSITÓRIO_REMOTO] [URL_REPOSITÓRIO_REMOTO]`;
	  - **Ex.:**
	  - `git remote add origin git@github.com:Paulo-E-F-Fernandes/configuracao-do-ambiente.git` para **SSH**;
	  - `git remote add origin https://github.com/Paulo-E-F-Fernandes/configuracao-do-ambiente.git` para **HTTPS**.
	- `git remote -v` - Para verificar os repositórios remotos adicionados;
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
    - E depois, para o **Bitbucket**:
      ```
      Host bitbucket.org
        Hostname altssh.bitbucket.org
        Port 443
      ```
	- Para o **GitHub**
	  ```
	  Host github.com
	    Hostname ssh.github.com
		Port 443
	  ```

> [Home](README.md)
