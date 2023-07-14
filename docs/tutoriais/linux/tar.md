---
tags:
  - Linux
  - Tar
---

# Tar
O comando "tar" é amplamente utilizado no Linux para compactar e descompactar arquivos em um único arquivo chamado "tarball".

## Compactar arquivos com o comando "tar"

Para compactar um diretório ou um conjunto de arquivos em um arquivo tar compactado, utilize o seguinte comando:

```shell
tar -czf /tmp/projetos.tar.gz Projetos/
```

## Descompactar arquivos com o comando "tar"
Para descompactar um arquivo tar, utilize o seguinte comando:

```shell
tar -xzf projetos.tar.gz
```


## Tabela de parametros
Aqui está uma tabela com alguns parâmetros comuns do comando "tar":


| Parametro | Descrição                                         |
| --------- | ------------------------------------------------- |
| -c        | cria um novo arquivo tar                          |
| -t        | exibe o conteúdo de um arquivo tar                |
| -p        | mantém as permissões originais do(s) arquivo(s);  |
| -r        | adiciona arquivos a um arquivo tar existente      |
| -f        | permite especificar o arquivo tar a ser utilizado |
| -v        | exibe detalhes da operação                        |


/// admonition | Alerta
    type: warning
Certifique-se de consultar a documentação do "tar" para obter mais informações sobre outros parâmetros e funcionalidades disponíveis.
///



Agora você está familiarizado com o comando "tar" para compactar e descompactar arquivos no Linux. Aproveite essas ferramentas para gerenciar seus arquivos de forma eficiente!