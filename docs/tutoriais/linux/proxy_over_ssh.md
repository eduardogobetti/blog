---
tags:
  - Linux
  - Proxy
---
# Proxy Over Ssh

## Criando o Túnel SSH

Abra o terminal no seu computador local e digite o seguinte comando:

```shell
ssh -X usuario@server -ND6969 -v
```

## Configurando o Navegador
* Abra as configurações do seu navegador.
* Procure por "Configurações de Rede" ou "Proxy".
* Selecione a opção "Usar proxy SOCKS" ou "SOCKS v5".
* Digite 127.0.0.1 como o endereço do proxy e 1080 como a porta.
* Salve as configurações.

<figure markdown>
  ![Image title](/assets/images/proxy_over_ssh.png){ align=left }
</figure>

