# Exercício de contribuição em um projeto onde você é colaboradora

- Se você já fez `clone` do repositório dessa a aula, então não precisa fazer de novo.
- Este exercício para casa segue o fluxo ao exercício que realizamos em [aula](https://github.com/reprograma/On8-git-github/blob/master/instrucoes/6-github-alunas.md).

### Instruções
#### Configurações básicas iniciais
* Ter o git instalado na sua máquina	
* Abra o Git Bash
  ```
  git --version
  ```
* Verifique se seu usuário está configurado na sua máquina. (Deve aparecer seu `user.name` e `user.email`)
	```
  git config --list
  ```

	* Caso não esteja configurado, fazer a configuração de `user.name` e `user.email`
    ```
    git config --global user.name "Seu Nome"
    git config --global user.email "seu@email.com"
    ```

---
#### Caso você precise fazer o fluxo do zero (desde o clone):

* Entre no Git Bash
* Verifique se está no diretório em que deseja clonar o repositório
	
  ```
  pwd
  ```
* Clonar o repositório desta aula
	
  ```
  git clone https://github.com/reprograma/On8-git-github.git
  ```

---

#### Caso você continue trabalhando no repositório já clonado durante a aula:
* Entrar nesse repositório local

	```
  cd On8-git-github/projeto
  ```
* Criar uma branch nova com seu nome.
	
  ```
  git checkout -b proj-seuNome
  ```
* Entrar no VSCode

	```
  code .
  ```
* Entrar na pasta `projeto` e siga as instruções.
* Alterar a imagem e o link para seu github na `<div>` que contiver seu nome.
	* Use o link do seu projeto do workshop para colocar no ***href*** na tag `<a>`. (Ex: https://github.com/cintiafumi/workshop-reprograma)
	* Use o link da imagem do seu avatar no github para colocar no ***src*** da tag `<img>`. Clique com o botão direito sobre a imagem do seu perfil no github e copie o endereço da imagem. (Ex: https://avatars0.githubusercontent.com/u/27314899?s=200&v=4)
    * Exemplo de como capturar o link da imagem:
      <img src="./img-readme/endereco-imagem.png">

  * Adicione seu nome no ***alt*** da tag `<img>`

  Exemplo:

    **Antes:**

    ```
      <div class="container__aluna">
        <a href="caminho do seu repo do workshop" target="_blank">
          <img class="container__aluna-img" src="https://via.placeholder.com/500" alt="Professora">
        </a>
        <p>Professora</p>
      </div>
    ```
    
    **Depois:**
    
    ```
      <div class="container__aluna">
        <a href="https://cintiafumi.github.io/workshop-reprograma/" target="_blank">
          <img class="container__aluna-img" src="https://avatars1.githubusercontent.com/u/34029172?s=460&u=87514f974accb262acd3ed1f3cd9553684b4d926&v=4" alt="Cintia Fumi">
        </a>
        <p>Cintia Fumi</p>
      </div>
    ```

* Conferir essa alteração no navegador (Chrome).
	* *Comportamento esperado: ao clicar na sua foto, o link do seu github irá se abrir numa aba nova*

* Voltando para o Git Bash.
* `git diff`: verificar o que você alterou no código.
* `git status`: verificar o status.
* `git add index.html`: Adicionar as alterações para área de preparação.
* `git status`: verificar o status novamente.
* `git commit -m "feat(github): foto de perfil e link para repo de Cintia Fumi"`: adicionar mensagem de ***commit***.
* `git push origin proj-seuNome`: subir as alterações da sua branch para o seu repositório remoto.
* Verificar se as alterações foram atualizadas na sua branch lá no github (https://github.com/reprograma/On8-git-github)
* Ir para a aba ***Pull requests***
* Criar novo pull request ***Compare & pull request*** pelo github da reprograma verificando se está fazendo a solicitação da proj-seuNome para a master
* *base: **master**    **<=**    compare: **proj-seuNome***
* Solicitar code review de 2 colegas

---

#### Após todos ***pull request*** dessa aula serem aceitos, caso queira atualizar localmente seu repositório:
* No Git Bash, dentro deste repositório.
* `git checkout master`: voltar para a branch master
* `git pull origin master`: atualizar o repositório local
* Verificar no navegador (Chrome) se todas as atualizações vieram

---
#### Deletar sua branch após seu ***pull request*** ser aceito
* `git checkout master`: estar na branch **master** para remover sua branch
* `git branch -D proj-seuNome`: deletar sua branch **proj-seuNome**

---
#### Para ter este repositório no seu GitHub, existem 2 alternativas:
- **Subindo como você subiu todos os seus projetos**
  * Criar um novo repositório no seu github https://github.com/new
  * Copiar o link do repositório.
  * `git remote add meuRepo https://github.com/<seuLogin>/<seuNovoRepositorio>.git`: adicionar o link remoto pelo Git Bash. (Como o remote origin já está linkado ao repositório da Reprograma, iremos adicionar o seu remote com outro nome). Obs: Nesse link acima, substituir `<seuLogin>` e `<seuNovoRepositorio>` com informações do seu login e seu repositório.
  * `git commit -m "Exercício para casa" --allow-empty`: fazer um ***commit*** vazio, pois tudo já foi adicionado anteriormente e não há novas alterações
  * `git push meuRepo master`: Subir esse repositório local no seu repositório do GitHub.

ou

- Fazendo um ***fork*** pelo próprio repositório da Reprograma;
  * Ir no repositório da Reprograma e clicar em ***Fork***
  <img src="./img-readme/fork.png">
