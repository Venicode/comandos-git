Idiomas: [Português](readme-br.md) | [Inglês](readme.md)

# 📚 Principais Comandos do GIT
Repositório para exempificar e resumir os principais comandos utilizados no GIT e qual situação serve cada um deles!

## ✨ Inicializando um repositório

Tendo o GIT instalado e configurado suas credenciais, basta abrir o Git Bash clicando com o botão direito do mouse em cima da pasta do seu projeto e inserir o comando abaixo:

```
git init
```

## ✔️ Conectando com o repositório remoto

Para vincular o repositório local com o remoto:

```
git remote add origin https://github.com/username/repositorio.git
```
<i> Substitua o link com o do seu repositório remoto.</i>

## ⚡ Clonando um repositório remoto

Caso já tenha um repositório criado e deseja apenas trazê-lo para a pasta do seu projeto:

```
git clone https://github.com/username/repositorio.git
```

## ➕ Adicionando conteúdo no staging

Antes de realizar um commit, você precisa adicionar as mudanças e novos arquivos na área de preparação (staging):

Adicionando um arquivo diretamente:

```
git add nome_arquivo
```
Adicionando um arquivo que está dentro de outra pasta:
```
git add pasta/nome_arquivo
```
Adicionando todas as mudanças realizadas:
```
git add .
```

## ➖ Removendo um arquivo do staging

O <b>git restore</b> remove os arquivos que foram inseridos no staging, mas <b>não desfaz as alterações nos arquivos do seu projeto.</b>

Caso tenha adicionando um arquivo errado no exemplo anterior, você pode retirá-lo:
```
git restore -- staged nome_arquivo
```
Se deseja remover todos os arquivos que tenha adicionado:
```
git restore -- staged .
```

## 🔍 Visualizando o status atual do seu repositório local

Para verificar quais arquivos já foram e não foram adicionados para o commit:
```
git status
```

O que está em vermelho são os arquivos que ainda não foram adicionados:

![exemplo_git_vermelho](images/image-6.png)

O que está em verde são os arquivos que já foram adicionados:

![exemplo_git_verde](images/image-5.png)

E caso não tenha nada novo para adicionar, aparecerá esta mensagem:

![exemplo_git_nada](images/image-8.png)

## 📦 Realizando um commit

Para realizar um commit, onde vai preparar todas as alterações adicionados para o envio ao repositório remoto:

```
git commit -m "sua mensagem do commit"
```
<i>Importante que sua mensagem explique qual mudança ou novo arquivo está adicionando ao seu projeto.</i>

## 🚀 Enviando seu commit através do push

Para enviar seu commit para o repositório remoto.

```
git push -u origin nome_branch
```
## 🔍 Visualizando o histórico de commits
Para visualizar todos os commits já feitos:

```
git log
```
## 📝 Alterando a mensagem do último commit
Para alterar a mensagem do último commit que foi feito:

```
git commit --amend -m "sua mensagem nova"
```
## ↩️ Desfazando um commit do HEAD
Para desfazer o último commit que foi feito sem desfazer as alterações dos arquivos no staging, apenas removendo o apontamento dele pelo HEAD (sempre aponta para último commit) e mantendo as alterações nos arquivos reais do seu projeto:

```
git reset --soft
```

## ↩️ Desfazando um commit do HEAD e staging
Para desfazer o último commit que foi feito desfazendo as alterações dos arquivos no staging e removendo o apontamento dele pelo HEAD (sempre aponta para último commit) e mantendo as alterações nos arquivos reais do seu projeto:

```
git reset --mixed
```
## ↩️❗ Desfazando um commit do HEAD, staging e as alterações do seu projeto
Para desfazer o último commit que foi feito desfazendo as alterações dos arquivos no staging e removendo o apontamento dele pelo HEAD (sempre aponta para último commit) e <b>removendo as alterações nos arquivos reais do seu projeto</b>:

```
git reset --hard
```

## ⬇️ Atualizando seu projeto local através do pull
Caso você ou outra pessoa que está trabalhando no mesmo projeto tenha feito alguma atualização e queira atualizar no seu repositório local:
```
git pull
```
## ➕ Criando uma nova branch

Pra criar uma nova branch:
```
git checkout -b nome_branch
```
## 🔨 Trocando de branch

Pra trocar de branch:
```
git checkout nome_branch
```
## 🔍 Visualizar o último commit de cada uma das branchs

Para verificar o último commit de cada uma das branchs criadas:

```
git branch -v
```

## ❌ Deletando uma branch

Para deletar uma branch criada:

```
git branch -d nome_branch
```

## 🔀 Realizando o merge entre duas branchs

Antes de realizar o merge, verifique se está na branch que vai receber as novas alterações. Após disso, execute o comando:
```
git merge branch_origem
```