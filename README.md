| **Lab**         |     **Data**   |
|  :----:     |  :----:    |
| Laboratório Ágil     | 2023       |

Guia de Instalacao do Docker - Windows
===
Guia para instalação e atualização do Docker para o Windows, descrevendo como instalar uma distribuição Linux no WSL2.

## Passo 1 - Atualizando o WSL

### 1.a - Windows 10 e Windows 11
Estas versões do Windows ja possuem o WSL instalado, porém ao rodar o comando ``wsl`` dentro do Prompt de Comando, teremos um aviso como o abaixo, dizendo que o wsl ainda não possui uma distribuição Linux associada para uso.

![image](https://user-images.githubusercontent.com/18387737/225308152-447da342-ebff-44e1-8bf8-f1034586c099.png)

Porém, antes de instalarmos uma distribuição, precisamos atualizar o WSL para ele utilizar por padrão as distribuições com arquitetura WSL2, que é a utilizada pelo Docker no Windows.

Para isso, primeiramente iremos rodar no prompt de comando(preferencialmente com permissão administrativa) o comando abaixo:

```
wsl --update
```
⚠️Caso esteja utilizando a Rede interna do Insper de Alunos ou Colaboradores, pode acontecer do download da atualização não iniciar dependendo do servidor da Microsoft em que a requisição de download chegar. Para evitar problemas, é recomendado executar os comandos deste passo do guia em uma Rede externa.

Após a conclusão da atualização, dando um novo comando ``wsl`` teremos uma tela como a abaixo:

![chrome_xXk1sh20bw](https://user-images.githubusercontent.com/18387737/225321510-0360b75e-9ae0-4ff8-98db-959e6da804dd.png)

Agora nosso WSL está atualizado para a arquitetura WSL2. Para instalar uma distribuição Linux, vamos utilizar o comando ``wsl.exe install <distribuição>``. Para saber o nome da distribuição que voçê quer instalar, podemos puxar uma lista dos subsistemas disponíveis com o comando abaixo:
````
wsl.exe --list --online
````
![image](https://user-images.githubusercontent.com/18387737/225322426-c473659e-8182-4f12-bf8e-8e95fdad961b.png)

Depois de escolher sua versão (por padrão, escolha o Ubuntu), basta trocar o campo ``<distribuição>`` do comando acima pelo nome da distribuição na primeira coluna da lista exibida:
````
wsl.exe install Ubuntu
````

Aguarde o fim da instalação, e então será pedido para você criar um usuário e senha para o subsistema. Anote em um lugar seguro o que você escolher caso seja necessário utilizar futuramente, mas agora seu WSL está pronto para ser utilizado pelo Docker. Caso ainda não tenha instalado ele no seu computador, siga para o passo 2.

### 1.b: Windows anteriores ao 10
Caso você esteja utilizando o Windows 8 ou anterior como seu OS, os passos acima podem não funcionar corretamente, então recomendamos seguir o guia da Microsoft para a instalação e atualização do WSL: https://learn.microsoft.com/pt-br/windows/wsl/install-manual

## Passo 2: Instalando o Docker no Windows



