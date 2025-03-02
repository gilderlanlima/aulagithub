# README - Principais Comandos Git para Subir um Projeto no GitHub

## 1. Configuração Inicial

Antes de começar, é importante configurar o Git com seu nome e e-mail:

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@example.com"
```

Isso garante que seus commits sejam identificados corretamente.

---

## 2. Criando um Repositório Local

Se você ainda não tem um repositório Git no seu projeto, inicialize um com:

```bash
git init
```

Isso criará uma pasta oculta `.git` no diretório do projeto, onde o Git armazenará todas as informações de versionamento.

---

## 3. Adicionando Arquivos ao Controle de Versão

Após criar ou modificar arquivos, adicione-os ao índice (staging area):

```bash
git add .
```

O ponto (`.`) indica que todos os arquivos modificados e novos serão adicionados.

---

## 4. Criando um Commit

Depois de adicionar os arquivos ao índice, é necessário criar um commit para registrar as mudanças:

```bash
git commit -m "Mensagem descritiva do commit"
```

A mensagem deve ser clara e objetiva sobre as alterações feitas.

---

## 5. Criando um Repositório no GitHub

Antes de enviar o projeto, você precisa criar um repositório no GitHub.

1. Acesse [GitHub](https://github.com/) e faça login.
2. Clique no botão **New repository**.
3. Defina um nome para o repositório e clique em **Create repository**.
4. Copie a URL do repositório remoto.

---

## 6. Conectando o Repositório Local ao GitHub

Agora, conecte seu repositório local ao repositório remoto:

```bash
git remote add origin https://github.com/seu-usuario/nome-do-repositorio.git
```

Substitua `seu-usuario` pelo seu nome de usuário e `nome-do-repositorio` pelo nome do repositório criado no GitHub.

---

## 7. Enviando os Arquivos para o GitHub

Para enviar os commits para o repositório remoto, utilize:

```bash
git push -u origin main
```

Se estiver utilizando a branch `master`, substitua `main` por `master`.

Caso seja o primeiro push, o `-u` define o repositório remoto como o padrão para futuros envios.

---

## 8. Clonando um Repositório Existente

Se quiser baixar um repositório do GitHub para seu computador, use:

```bash
git clone https://github.com/seu-usuario/nome-do-repositorio.git
```

Isso criará uma cópia do repositório no seu diretório atual.

---

## 9. Atualizando o Repositório Local com Alterações Remotas

Se houver mudanças no repositório remoto feitas por outra pessoa, atualize seu repositório local com:

```bash
git pull origin main
```

Isso baixa e mescla as alterações mais recentes.

---

## 10. Verificando o Status do Repositório

Para verificar quais arquivos foram modificados ou estão prontos para commit, utilize:

```bash
git status
```

---

## 11. Verificando o Histórico de Commits

Para visualizar os commits realizados no repositório, use:

```bash
git log
```

Você pode pressionar `q` para sair do histórico.

---

## 12. Criando e Mudando de Branch

Para criar uma nova branch:

```bash
git branch nome-da-branch
```

Para mudar para outra branch:

```bash
git checkout nome-da-branch
```

Ou para criar e mudar de branch ao mesmo tempo:

```bash
git checkout -b nome-da-branch
```

---

## 13. Mesclando Branches

Se quiser unir uma branch à branch principal (`main` ou `master`):

```bash
git checkout main  # Vá para a branch principal
git merge nome-da-branch  # Mescle a branch desejada
```

---

## 14. Removendo uma Branch

Para deletar uma branch local:

```bash
git branch -d nome-da-branch
```

Para deletar uma branch no repositório remoto:

```bash
git push origin --delete nome-da-branch
```

---

## 15. Ignorando Arquivos no Git

Se quiser evitar que determinados arquivos sejam versionados, crie um arquivo `.gitignore` e adicione os arquivos ou pastas que deseja ignorar. Exemplo:

```
/node_modules/
.env
.DS_Store
```

---

## Conclusão

Agora você conhece os principais comandos do Git para subir um projeto no GitHub e gerenciar o versionamento do seu código. Pratique regularmente para se familiarizar com o fluxo de trabalho!
