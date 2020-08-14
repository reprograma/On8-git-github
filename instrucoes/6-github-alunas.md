### Contribuindo com um projeto da Reprograma
- Entrar o repositório do projeto da Reprograma: https://github.com/reprograma/On8-git-github
- Copiar o link HTTP que aparece ao clicar no botão verde ***Clone or download***.
- Na sua máquina: abrir o Git Bash clicando com o botão direito do mouse de dentro da pasta onde deseja clonar o repositório (*Git Bash here*).
- `git clone https://github.com/reprograma/On8-git-github.git`
- `cd On8-git-github`: para entrar na pasta.
- `ls`: para listar o que tem dentro da pasta.
- `git branch -a`: para listar as branch's que tem nesse projeto.
- `git checkout -b aula-seuNome`: para ir para uma branch nova chamada aula-seuNome.
- `code .`: para abrir o VSCode nessa pasta.
- Abrir o arquivo `index.html` da pasta `aula` no seu navegador (Chrome).
- No VSCode, verificar se está na sua branch pela parte inferior esquerda do VSCode.
- Alterar o código colocando `seu login GitHub` na `<td>` abaixo do seu nome.
  Exemplo:

  **Antes:**
    ```
        <tr>
          <td>Professora</td>
          <td>
            <a href="https://github.com/seuLoginGitHub" target="_blank">
              Seu login GitHub
            </a>
          </td>
        </tr>
    ```

  **Depois**
    ```
        <tr>
          <td>Cintia Fumi</td>
          <td>
            <a href="https://github.com/cintiafumi" target="_blank">
              cintiafumi
            </a>
          </td>
        </tr>
    ```
    
- Salve a alteração e verifique no navegador se está correto.
- Volte para o Git Bash dentro dessa pasta.
- `git diff`: verifique o que foi modificado.
- `git status`: verifique o status do repositório atual.
- `git add --all`: adicione todos os arquivos que foram modificados.
- `git commit -m "Mensagem de bom senso"`: adicionando a mensagem do que foi modificado.
- `git remote -v`: verifique se o endereço do repositório remoto. (Neste caso, o endereço do remoto chamado `origin` já veio quando você fez o clone do repositório).
- `git push origin aula-seuNome`: envie para o repositório remoto as alterações da branch `aula-seuNome`.
- Verifique no GitHub se sua alteração foi enviada com sucesso. Veja se sua branch está no repositório: https://github.com/reprograma/On8-git-github
- Clicar na aba **Pull requests** do repositório no GitHub.
- Clicar em **Compare & pull request** e verifique as alterações no código.
- **base: master <= compare: aula-seuNome**: Criar o **pull request** verificando se está indo da sua branch `aula-seuNome` para a branch master.
- Solicitar a revisão de código para a professora **cintiafumi** e duas colegas.
- Aguardar a aprovação da sua solicitação.
- A professora fará o **merge** da sua branch `aula-seuNome` para a `master`.
