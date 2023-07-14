---
tags:
  - Linux
  - ssh
---
# ssh-keygen

Gerar e Copiar Chaves SSH com o `ssh-keygen`
o `ssh-keygen` é uma ferramenta utilizada para gerar pares de chaves SSH para autenticação segura em servidores remotos. 
Neste tutorial, você aprenderá como gerar uma nova chave SSH e como copiá-la para um servidor.


## Gerar uma Nova Chave SSH
Para gerar uma nova chave SSH com o `ssh-keygen`, execute o seguinte comando:

```shell
ssh-keygen -t ed25519 -C "comentario" -f ~/.ssh/nome.usuario
```
/// admonition | Alerta
    type: warning
  Certifique-se de substituir "comentario" pelo seu próprio comentário e 
  "nome.usuario" pelo nome de arquivo que deseja atribuir à chave.
///

## Copiar a Chave para o Servidor
Existem duas maneiras comuns de copiar a chave para o servidor remoto: usando ssh-copy-id ou fazendo manualmente.

### Usando ssh-copy-id
Para copiar a chave para o servidor usando ssh-copy-id, utilize o seguinte comando:

```shell
ssh-copy-id -i ~/.ssh/mykey user@host
```
/// admonition | Alerta
    type: warning
  Certifique-se de substituir mykey pelo nome do arquivo da chave SSH que 
  você gerou e "user@host" pelas suas próprias credenciais de acesso ao servidor.
///

### Copiar a Chave Manualmente
Se preferir copiar a chave manualmente, siga os passos abaixo:

```shell
scp ~/.ssh/id_rsa.pub user@host:~/

ssh user@host

mkdir .ssh
chmod 700 .ssh

touch .ssh/authorized_keys 
chmod 644 .ssh/authorized_keys

cat id_rsa.pub >> .ssh/authorized_keys
```
/// admonition | Alerta
    type: warning
  Certifique-se de substituir user@host pelas suas próprias credenciais de acesso ao servidor.
///

