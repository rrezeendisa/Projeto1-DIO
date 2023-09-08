# Projeto1-DIO
 Projeto do Curso Git e GitHub da Plataforma DIO
# Projeto DIO 1

Repositório para mostrar os conhecimentos básicos sobre Git e GitHub aprendidos pela plataforma [Digital Innovation One](https://web.dio.me/course/versionamento-de-codigo-com-git-e-github/learning/599dd3dd-d189-474f-a55c-22f37b4472da?back=/track/santander-bootcamp-2023-fullstack-java-angular&tab=undefined&moduleId=undefined). Nesse README, irá conter algumas documentações sobre Git e GitHub. Repositório aberto para sugestões, correções e aprendizados.

## ⚠️Documentação
- [Documentação Git](https://git-scm.com/doc)
- [Documentação GitHub](https://docs.github.com/)
- [Site que me auxiliou no resumo também](https://www.atlassian.com/br/git/tutorials/setting-up-a-repository#:~:text=Para%20criar%20um%20novo%20repositório,no%20diretório%20de%20trabalho%20atual.)

## 💻Temas abordados nas aulas
| Nº da aula | Tema |
|-------|---------|
|02| O que é versionamento de código?|
|03| O que é Git?|
|04| O que é GitHub|
|07| Configurando o Git|
|08| Autenticando via Token|
|09| Autenticando via chave SSH|
|10| Criando e clonando repositórios|
|11| Salvando Alterações no Repositório Local|
|12| Desfazendo Alterações no Repositório Local|
|13| Enviando e Baixando Alterações com o Repositório Remoto|

## ❓ O que é versionamento de código?
O versionamento é um gerenciador de código e Scripts. Ele é muito necessário para o desenvolvimento, aplicação e correção de softwares. Geralmente usado pelos desenvolvedores, com a intenção de não só ter controle pelo histórico de seus códigos, mas também para que assim o compartilhamento de código seja mais prático.

## ❓ O que é Git e o que é GitHub?
**Git:**
O Git nada mais é do que um sistema de controle de versão DISTRIBUÍDO, ou seja, o programa será duplicado localmente, então os desenvolvedores vão ter acesso ao código para editá-lo, mesmo que o servidor esteja fora do ar. Por ser gratuito, Open Source (código aberto) e mais popular que os demais, os desenvolvedores acabam optando por ultilizar ele.

**GitHub:**
Mesmo tendo um nome "parecido" com o anterior, o GitHub é uma plataforma de hospedagem de código para controle de versão JUNTAMENTE com o Git. O GitHub tem uma comunidade ativa e é utilizado MUNDIALMENTE.

A principal diferença entre os dois, é que o Git vai atuar gerenciando o banco de versões de seus programas, já o GitHub vai hospedar o seu programa remoto.


## ⌨️ Configurando o Git

| Comando | Função |
|---------|--------|
|Git config| Permite vizualizar e definir variáveis de configuração do Git|
|Git config - global| Configuração do usuário|
|Git config - system | Configuração do sistema Windows|
|Git config - local | Configuração do repositório|
|Git Init| Inicializa |
|Git config Init.defaultBranch | Mostra a Branch padrão |

## ❓ O que é autenticação via Token? E como autenticar?
A autenticação via Token serve para autenticar uma conta de uma forma mais segura. Ele contém as informações sobre a identidade do principal que faz a solicitação e para que tipo de acesso ele está autorizado. Ela não é usada somente no GitHub, a maiorias das grandes empresas voltada a tecnologia utilizam esse meio de segurança, como a Google e a Amazon.

**PARA AUTENTICAR O GIT VIA TOKEN, SEGUE OS PASSOS:**

Login no GitHub -> Página principal -> Clique no botão superior direito -> Clique em Settings -> Developer settings (18º opção na lista) -> Personal access tokens -> Generate New Token -> Confirme a sua senha do GitHub -> Digite o nome para o seu Token e insira o tempo de expiração nas opções -> Marque as opções desejadas para conceder a esse Token, mas a opção **repo** SEMPRE vai estar selecionada, para que assim seja concedido esse Token ao seu repositório -> Generate token.

## ❓ O que é chave SSH e como autenticar?

SSH significa Security Shell - é um protocolo de rede que possibilida que o computador e o servidor (GitHub) se conectem de forma mais segura e criptografada, por meio da internet. A SSH, trabalha com duas chaves: Pública e Privada. A Pública vai ser utilizada para se conectar entre o Git e o GitHub, já a privada, é a sua senha, onde somente o criador, pode ter acesso a ela.

**Gerando nova chave SSH**
Entre no GitHub -> Página principal -> botão superior direito -> settings -> Acess -> SSH and GPG Keys -> Link do SSH -> Verificar se há chaves SSH -> Sobre SSH -> Add o título/nome da chave -> Permaneça como Key Type -> Adicione sua chave Pública (gerada em seu Git).

##❓ Como gerar chave no Git?
Abra o Git Bash -> Cole o exemplo a seguir, substituindo o exemplo pelo seu e-mail: 
```
ssh-keygen -t ed25519 -C "your_email@example.com"
```
-> Usando o email, será criado uma nova chave SSH
```
> Generating public/private ALGORITHM key pair.
```
-> Quando for solicitado a inserir um arquivo para salvar a chave, pressione Enter para aceitar o local padrão do arquivo. Observe que, se você criou chaves SSH anteriormente, ssh-keygen pode pedir que você reescreva outra chave. Nesse caso, recomendamos criar uma chave SSH personalizada. Para fazer isso, digite o local do arquivo padrão e substitua id_ssh_keyname pelo nome da chave personalizada.
```
>  Enter a file in which to save the key (/c/Users/YOU/.ssh/id_ALGORITHM):[Press enter]
```
-> Já no Prompt, digite uma nova senha segura
```
> Enter passphrase (empty for no passphrase): [Type a passphrase]
> Enter same passphrase again: [Type passphrase again]
```
**Add a nova chave SSH ao ssh-agente**
-> Verifique se o ssh-agent está em execução com o seguinte comando: 
```
# start the ssh-agent in the background
$ eval "$(ssh-agent -s)"
> Agent pid 59566
```
-> Add a sua nova chave privada ao ssh-agent. Caso já tenha criado sua chave com nome diferente ou criou sua chave com um nome diferente, substitua o *id_ed25519* no comando pelo nome do arquivo da chave privada *shell ssh-add ~/.ssh/id_ed25519.



## ⚠️ Criando e Clonando um repositório

**DICA:** Já tenha salvo a pasta na qual você deseja criar o repositório.

-> Para criar um novo repositório, você vai começar usando o comando *git init*. Esse comando vai transmormar o diretório atual em um novo repositório Git vazio;
-> Adicione arquivos nesse seu novo repositório, copiando os arquivos para o diretório do repositório OU adicionando o comando *git add*, assim, você vai add arquivos específicos;
-> Faça uma captura do estado atual dos arquivos do repositório. Para isso, use a função *git commit*.
Ex.:
```
git commit -m "Exemplo de commit"
```
*Troque o que está entre aspas ("") por o que está sendo mudado no commit.
-> Por fim, compartilhe ao seu GitHub!



```
Dio.me
```

## Referencias

