---
title: "GPGME error: No data. Como resolver?"
date: 2022-05-02T08:35:30-03:00
categories:
  - Linux
  - Archlinux
  - Bugs
tags:
  - linux
  - archlinux
  - gpg
  - pacman
---
## O Erro ###
Você vai tentar atualizar o sistema ou instalar um pacote e quando você vai dar ENTER aparece a seguinte mensagem abaixo no seu terminal:
```
error: GPGME error: No data
error: GPGME error: No data
error: GPGME error: No data
error: GPGME error: No data
error: GPGME error: No data
:: Synchronizing package databases…
basis is up to date
platform is up to date
addon is up to date        0.0   B  0.00B/s 00:00 [———————-]   0%
extra is up to date        0.0   B  0.00B/s 00:00 [———————-]   0%
community is up to date    0.0   B  0.00B/s 00:00 [———————-]   0%
basis-multilib is up to date.0   B  0.00B/s 00:00 [———————-]   0%
multilib is up to date     0.0   B  0.00B/s 00:00 [———————-]   0%
error: database ‘addon’ is not valid (invalid or corrupted database (PGP signature))
error: database ‘extra’ is not valid (invalid or corrupted database (PGP signature))
error: database ‘community’ is not valid (invalid or corrupted database (PGP signature))
error: database ‘basis-multilib’ is not valid (invalid or corrupted database (PGP signature))
error: database ‘multilib’ is not valid (invalid or corrupted database (PGP signature))
```
Que erro é esse?
## O Problema ##
A base de dados do seu sistema está inválida ou corrompida, com isso impossibilita de fazer atualizaçãoes ou até mesmo instalar um novo pacote.
## A Solução ##
E para resolver, faça da seguinte forma:
```
$ sudo rm /var/lib/pacman/sync/*
$ sudo pacman-key –init
$ sudo pacman-key –populate archlinux manjaro
$ sudo pacman -Syy
```
