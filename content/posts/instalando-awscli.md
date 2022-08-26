---
title: "Instalando AWS CLI no Linux"
date: 2022-08-26T18:22:47-03:00
author: "Hector Filipy"
cover:
     image: /images/AWS-CLI.png
     alt: 'Capa publicação'
tags: ["AWS", "CLI", "AMAZON", "LINUX"]
categories: ["Tutorial"]
---

# Instalando AWS CLI

Fala galerinha tudo bem?

Hoje vamos aprender a instalar o AWS CLI no Linux... no final teremos um bônus para instalação no Windows e MacOS.

# Linux

* Requisitos de Instalação:
  - Será necessário algum programa de descompactação de arquivos, aqui vamos usar o unzip, mas pode ser usado um equivalente.
  - A AWS CLI precisará do glibc, groff e less. Geralmente já é nativo nas principais distribuições Linux.
  - A AWS CLI é utilizada na versão 64 bits, e pode ser utilizado nas distribuições recentes do CentOS, Fedora, Ubuntu, Amazon Linux 1, Amazon Linux 2 e Linux ARM.
  - A AWS não utiliza software de terceiros, com isso não é garantido que terceiros tenham a versão mais recente.

* Instalação ou atualização do AWS CLI

Vamos executar os comandos abaixo para instlar a AWS CLI no Linux.

```bash
$ curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
```
Logo em seguida iremos descompactar os arquivos digitando o comando abaixo...

```bash
unzip awscliv2.zip
```
Após descompactar o arquivo, iresmo digitar o comando a seguir...

```bash
sudo ./aws/install
```

E para validarmos se a instalação ocorreu bem vamos digitar o comando:

```bash
$ aws --version
```

A saída deve ser algo como:

```texto
aws-cli/2.4.5 Python/3.8.8 Linux/4.14.133-113.105.amzn2.x86_64 botocore/2.4.5
```

# MacOS e Windows

As instalações no MacOS e Windows são relativamente mais fáceis, pois existe a possibilidade de instalação no modo GUI, onde é só baixar o pacote, executar e seguir o passo a passo de cada janela... mais para qualquer dúvida vou deixar o link da AWS caso vocês queiram instalar nessas plataformas...

* [Instalar ou Atualizar a versão mais recente da AWS CLI](https://docs.aws.amazon.com/pt_br/cli/latest/userguide/getting-started-install.html)

