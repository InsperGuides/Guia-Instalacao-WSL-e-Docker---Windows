| **Lab**         |     **Data**   |
|  :----:     |  :----:    |
| Laboratório Ágil     | 2023       |

Guia de Instalacao do Docker - Windows
===
Guia para instalação e atualização do Docker para o Windows, descrevendo como instalar uma distribuição Linux no WSL2.

## Passo 1 - Atualizando o WSL

### 1.a - Windows 10 e Windows 11
Estas versões do Windows ja possuem o WSL instalado, porém ao rodar o comando *wsl* dentro do Prompt de Comando, teremos um aviso como o abaixo, dizendo que o wsl ainda não possui uma distribuição Linux associada para uso.

![image](https://user-images.githubusercontent.com/18387737/225308152-447da342-ebff-44e1-8bf8-f1034586c099.png)

Porém, antes de instalarmos uma distribuição, precisamos atualizar o WSL para ele utilizar por padrão as distribuição que utilizam a arquitetura do WSL2, que é a utilizada pelo Docker no Windows.

Para isso, primeiramente iremos rodar no prompt de comando(preferencialmente com permissão administrativa) o comando abaixo:

```
wsl --update
```

:warning:

