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
⚠️Caso esteja utilizando a Rede interna do Insper de Alunos ou Colaboradores, pode acontecer do download da atualização não iniciar dependendo do servidor da Microsoft em que a requisição de download chegar. Para evitar problemas, é recomendado executar os comandos do WSL em uma Rede externa.

Após a conclusão da atualização, dando um novo comando *wsl* teremos uma tela como a abaixo

![image](https://user-images.githubusercontent.com/18387737/225309711-15963b1b-9880-487e-9724-d26b7aeec338.png)

Agora nosso WSL está atualizado para a arquitetura WSL2.

