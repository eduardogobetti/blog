---
tags:
  - Linux
  - Zsh
---
# Oh My Zsh

Oh My Zsh é um framework de gerenciamento de configuração do Zsh (um shell poderoso para a linha de comando no Linux e macOS). Ele vem com uma série de recursos e temas úteis que tornam a experiência de linha de comando mais eficiente e agradável.


## Instalando o Zsh

No Ubuntu, você pode usar o gerenciador de pacotes apt para instalar o Zsh:

```shell
sudo apt install zsh git -y
```

## Instalando o Oh My Zsh
Agora que o Zsh está instalado, vamos instalar o Oh My Zsh. Digite o seguinte comando em seu terminal:

```shell
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
O script de instalação irá clonar o repositório do Oh My Zsh do GitHub e configurá-lo para você.

## Alterando o Tema
O Oh My Zsh vem com diversos temas para personalizar a aparência do seu prompt de comando. 
### Listar Temas
```shell
omz theme list
```
### Setar Tema
```shell
omz theme set agnoster
```