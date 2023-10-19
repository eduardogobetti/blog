---
tags:
  - Linux
  - Rsync
---
# Rsync

O `rsync` é uma poderosa ferramenta de transferência de arquivos e sincronização disponível em sistemas Linux e Unix. Ele é amplamente utilizado para copiar e sincronizar arquivos e diretórios localmente ou entre máquinas remotas de forma eficiente.

## Sintaxe básica
```shell
rsync opções origem destino
```

## Exemplos práticos

### 1. Copiando um arquivo localmente

Para copiar um arquivo de origem para um destino local, você pode usar o comando:

```shell
rsync -av origem/arquivo.txt destino/
```

- `-a`: ativa o modo arquivo, que preserva permissões, timestamps, links simbólicos etc.
- `-v`: ativa o modo verbose para exibir informações detalhadas sobre o processo.

### 2. Sincronizando diretórios localmente

Para sincronizar o conteúdo de um diretório de origem com um diretório de destino localmente, você pode usar o seguinte comando:

```shell
rsync -av origem/ destino/
```


### 3. Copiando para um servidor remoto

Para copiar arquivos ou diretórios para um servidor remoto usando SSH, utilize o seguinte formato:

```shell
rsync -av origem/ usuario@servidor:/caminho/destino/
```

- `usuario`: substitua pelo nome do usuário no servidor remoto.
- `servidor`: substitua pelo endereço ou nome do servidor remoto.

### 4. Excluindo arquivos e diretórios

Você pode excluir arquivos ou diretórios específicos durante a transferência usando a opção `--exclude`. Por exemplo:

```shell
rsync -av --exclude 'arquivo.txt' origem/ destino/
```