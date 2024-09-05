# 📚 Principais Comandos do GIT
Repositório para exempificar e resumir os principais comandos utilizados no GIT e qual situação serve cada um deles!

## ✨ Inicializando um repositório

Tendo o GIT instalado e configurado suas credenciais, basta abrir o Git Bash e inserir o comando para inicializar o git dentro da pasta do seu projeto:

```
git init
```

## ✔️ Conectando com o repositório remoto

Para vincular o repositório local (sua máquina) com o repositório remoto (GitHub ou outra plataforma de hospedagem):

```
git remote add origin https://github.com/username/repositorio.git
```
<i> Exemplo com o GitHub (substitua o link com o do seu repositório remoto).</i>

## ⚡ Clocando um repositório remoto

Caso já tenha um repositório criado e deseja apenas trazê-lo para a sua máquina:

```
git clone https://github.com/username/repositorio.git
```

## ➕ Adicionando conteúdo para o commit

Antes de realizar um commit, você precisa adicionar as mudanças e novos arquivos que deseja mandar para o repositório remoto:

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

## ➖ Removendo uma alteração (apenas para não ir para o commit)

O <b>git restore</b> remove os arquivos que foram inseridos para o próximo commit, mas <b>não desfaz as alterações nos arquivos do seu projeto.</b>

Caso tenha adicionando um arquivo errado no exemplo anterior, você pode retirá-lo:
```
git restore -- staged nome_arquivo
```
Se deseja remover todos os arquivos que tenha adicionado:
```
git restore -- staged .
```

## 🔍 Verificando o status atual do seu repositório local

Para verificar quais arquivos já foram e não foram adicionados para o commit:
```
git status
```

O que está em vermelho são os arquivos que ainda não foram adicionados:

![exemplo_git_vermelho](image-6.png)

O que está em verde são os arquivos que já foram adicionados:

![exemplo_git_verde](image-5.png)

E caso não tenha nada novo para adicionar, aparecerá esta mensagem:

![exemplo_git_nada](image-8.png)

## 📦 Realizando um commit

Para realizar um commit, onde vai preparar todas as alterações adicionados para o envio ao repositório remoto:

```
git commit -m "sua mensagem do commit"
```
<i>Importante que sua mensagem explique qual mudança ou novo arquivo está adicionando ao seu projeto.</i>

## 🚀 Enviando seu commit através do push

Para enviar seu commit para o repositório remoto:
```
git push
```