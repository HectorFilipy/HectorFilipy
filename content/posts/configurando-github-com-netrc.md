---
title: "Configurando Github com .netrc"
date: 2022-08-22T19:42:23-03:00
author: "Hector Filipy"
---

# Configurando Git no .netrc

Vamos lá pessoal

Aqui voce aprenderá:

* Como fonfigurar o GitHub para não ficar pedindo a senha a cada push/pull

É muito importante dizer que existem outro métodos para realizar a autenticação, como por exemplo utilizar o SSH do git. Mas hoje vamos aprender a configurar o .netrc para não precisar ficar pedindo o usuário e senha.

## Configurando

Vamos criar um arquivo na pasta /home/seu-usuario

```bash
touch .netrc
```

Esse arquivo será criado e o .(ponto) deixará ele oculto

**OBS: É importante criar na pasta **home** do seu usuário ou do usuário que irá rodar o PUSH/PULL.**

Após criado o arquivo iremos editar ele digitando o seguinte comando:

```bash
cat .netrc
```

E iremos adicionar as seguintes linhas

```bash
machine github.com
login seu-login
password sua-senha
```

## Testando a configuração

Para realizar o teste e validar se está funcionando basta realizar o commit para subir as alterações e aplicar o push.

```bash
git add .
git commit -m "Comentário da alteração"
git push origin master
```

**OBS: No caso vamos aplicar a branch master, se voce estiver utilizando outra branch basta apontar para a branch desejada.**

## Entendendo o .netrc

O entendimento sobre o que se foi preenchido no arquivo .netrc é bem simples...

```bash
machine endereço // Neste campo será adicionado o endereço do servidor pra onde deseja realizar o push/pull.
login usuario // Neste campo será colocado o usuário a ser utilizado.
password senha // Neste campo será colocado a senha do usuário acima.
```

