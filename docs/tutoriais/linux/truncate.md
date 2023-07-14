---
tags:
  - Linux
  - Truncate
---
# Truncate

O comando "truncate" é uma ferramenta de linha de comando que permite reduzir ou estender o tamanho de um arquivo para um determinado valor.

A sintaxe geral para truncar um arquivo para tamanho zero com o comando "truncate" é a seguinte:

```shell
truncate -s 0 filename
```

## Truncate com “cat”
Outra forma de truncar um arquivo para tamanho zero é utilizando o comando "cat":

```shell
cat /dev/null > filename
```
## Truncate com “echo”
Você também pode utilizar o comando "echo" para truncar um arquivo para tamanho zero:


```shell
echo -n > filename
```

## Truncate com echo deixando as ultimas 500 linhas
Se você deseja manter apenas as últimas 500 linhas de um arquivo e descartar o restante, você pode usar o comando "echo" combinado com o comando "tail":

```shell
echo "$(tail -500  arquivo.log)"  >  arquivo.log
```