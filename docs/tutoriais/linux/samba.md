---
tags:
  - Linux
  - Samba
---
# Samba
O Samba é uma implementação do protocolo SMB/CIFS utilizado para compartilhar arquivos e impressoras entre sistemas Windows e Linux. Neste tutorial, você aprenderá como adicionar um usuário ao Samba e testar o acesso a um compartilhamento.

## **Adicionar um Usuário no Sistema Operacional**

Antes de adicionar um usuário ao Samba, é necessário adicioná-lo ao sistema operacional. Para isso, execute os seguintes comandos:

```shell
sudo useradd nome.do.usuario 
sudo passwd nome.do.usuario 
```

/// admonition | Alerta
    type: warning
  Certifique-se de substituir "nome.do.usuario" pelo nome de usuário desejado.
///

## **Adicionar um Usuário ao Samba**
Para adicionar um usuário ao Samba, utilize o comando smbpasswd da seguinte maneira:
```shell
sudo smbpasswd -a nome.do.usuario 
```
/// admonition | Alerta
    type: warning
  Lembre-se de substituir "nome.do.usuario" pelo nome de usuário escolhido anteriormente.
///

## **Adicionar um Usuário ao Grupo "docs"**
Caso seja necessário adicionar o usuário a um grupo específico, como o grupo "docs", utilize o comando usermod:

```shell
sudo usermod -G docs nome.do.usuario 
```

/// admonition | Alerta
    type: warning
  Lembre-se de substituir "nome.do.usuario" pelo nome do usuário e "docs" pelo nome do grupo desejado.
///

## **Testar o Acesso a um Compartilhamento**
Para testar o acesso a um compartilhamento do Samba, utilize o seguinte comando:

```shell
smbclient -U nome.do.usuario "//servidor.local/diretorio" -c dir
```
/// admonition | Alerta
    type: warning
Certifique-se de substituir "nome.do.usuario" pelo nome de usuário 
e "//servidor.local/diretorio" pelo caminho do compartilhamento desejado.
///