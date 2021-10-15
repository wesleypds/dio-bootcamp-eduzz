# <span class="underline">Entendendo o que é Git e sua importância</span>

-   **O que é?**

O Git é uma ferramenta que apoia no controle de versões de um determinado software que esteja em desenvolvimento, fazendo com que seja criada versões diferentes do software para cada mudança feitas nele.

-   **Git é GitHub?**

O Git e o GitHub são ferramentas diferentes, o Git irá controlar o versionamento do software, já o GitHub, será onde o código do software, suas mudanças e novas versões será hospedado, GitHub é uma espécie de repositório.

-   **Como operar o Git?**

O Git é um software que funciona por linhas de comandos (CLI), geralmente os comandos são executados no cmd ou terminal de algum editor de código.

### <span class="underline">Alguns comandos básicos para trabalhar com Git</span>

-   **Mudar de pastas:**

Windows = cd;

Unix (Linux, Mac) = cd.

Ex: Digitar o comando **cd \\** no cmd/terminal irá voltar para a base do **C:**, com isso digitando o comando **dir** irá listar as pastas/arquivos do **C:** e para entrar em uma pasta basta digitar o comando **cd nomeDaPasta.**

Para retrocedor 1 nível, basta digitar o comando **cd ..** tanto no windows quanto nos sistemas baseados em unix.

![](media/image1.png){width="4.091666666666667in" height="3.3409722222222222in"}

-   **Listar as pastas:**

Windows = dir;

Unix (Linux, Mac) = ls.

Ex: Digitar tanto **dir** quanto **ls** no cmd/terminal irá listar todas as pastas/arquivos existentes na pasta **C:\\Users\\jubil**.

![](media/image2.png){width="4.097916666666666in" height="2.803472222222222in"}

-   **Criar pastas/arquivos:**

Windows = mkdir;

Unix (Linux, Mac) = mkdir.

Ex: Digitando o comando **mkdir** irá criar uma pasta no atual diretório, para verificar se a pasta realmente foi criada basta digitar o comando **dir**. Obs: Geralmente quando ocorre algum erro é mostrado na tela do cmd que houve algum erro.

![](media/image3.png){width="4.090972222222222in" height="3.2416666666666667in"}

O comando **echo** irá printar uma mensagem na tela do cmd, para que se possa passar essa mensagem para um arquivo basta digitar no cmd **echo mensagem \> mensagem.txt**, com isso será criado um arquivo com o nome **mensagem.txt** e salvara nesse arquivo o texto **mensagem**.

O comando **mv nomeDoArquivo.md ./nomeDaPasta/** irá fazer com que o arquivo seja movido para dentro da pasta **nomeDaPasta**.

-   **Deletar pastas/arquivos:**

Windows = del / rmdir;

Unix (Linux, Mac) = rm -rf.

Ex: Digitando o comando **del workspace**, irá deletar os arquivos que existem dentro da pasta **workspace** quando você digitar **S** , de sim para confirmar.

![](media/image4.png){width="4.675694444444445in" height="0.7881944444444444in"}

Ex: Para excluir de fato a pasta mais todos os arquivos dentro desta pasta, basta digitar no cmd o comando **rmdir nomeDaPasta /S /Q.**

![](media/image5.png){width="4.740277777777778in" height="3.4972222222222222in"}

### <span class="underline">Tópicos fundamentais para entender o funcionamento do Git</span>

**4 tópicos:**

-   **SHA1:**

    É um algoritmo de criptação, ele gere uma chave com um conjunto de caracteres com 40 caracteres.

    Ex: Comando **openssl sha1 texto.txt** irá gerar uma chave de criptação para o arquivo **texto.txt**.

![](media/image6.png){width="4.761111111111111in" height="1.09375in"}

-   **Objetos fundamentais:**

1.  **BLOBS:**

    Contém nos Blobs o tipo, o tamanho da string, a instrução \\0 e o conteúdo em si, que está dentro desse Blob.

2.  **TREES:**

    As Trees armazena Blobs, e o nome do arquivo e tem um sha1 dos metadados desse objeto.

3.  **COMMITS:**

    Os commits apontam para as trees, parentes (que são commits feitos anteriormente), autor e a mensagem. Commit também possui um sha1.

-   **Sistema distribuído:**

    O Git é um sistema distribuido, que por sua vez, se algo acontecer com o servidor que está hospedando um código, todos os commiters desse código será afetado.

-   **Segurança:**

    A segurança do Git se passa pelo fato de que um commit é muito dificil ou até mesmo impossivel de ser adulterado por outra pessoa, por conta das criptações sha1.

**<span class="underline">Chave SSH e Token</span>**

**Processos para se autenticar:**

-   **Chave SSH:**

Se usa uma chave pública para que a máquina pessoal possa se conectar com um repositório de códigos (GitHub), com isso podendo fazer um push de um código sem precisar a validação de uma senha.

**Gerando uma chave SSH:**

Comando: **ssh-keygen -t nomeDaChave -C email\@email.com.**

Será pedido no processo de criação da chave, uma senha para poder validar essa chave no futuro.

**Encontrar a chave SSH:**

1° Comando: **cd /c/Users/usuario/.ssh/**

2° Comando: **ls** para listar os arquivos da pasta **.ssh**.

3° Comando: **cat nomeDaChave.pub** para acessar o arquivo da pasta **nomeDaChave** que será a sua chave pública.

**Validar a chave para que ela possa ser usada:**

1° Comando: **eval \$(ssh-agent -s)**.

2° Comando: **ssh-add nomeDaChave**.

Será pedido a senha criada no processo de criação da chave.

-   **Token:**

Token de acesso pessoal é uma chave gerada na hora pelo o GitHub que substituirá o login e senha na hora de se fazer um Commit.

### <span class="underline">Trabalhando com o Git e criando um Commit</span>

-   **Git init:**

O Git init irá inicializar um repositório vazio dentro da pasta que o comando **git init**

foi executado. Neste caso, irá criar uma pasta oculta chamada **.git .**

Para conseguir ler o conteúdo desta pasta deverá ser executado o comando **ls -a**.

-   **Git add:**

O Git add irá prepapar os arquivos para que sejam commitados, se é necessário commitar todos os arquivos da pasta, basta executar o comando **git add \***, o \'\*\' irá indicar que você está querendo commitar todos os arquivos da pasta.

-   **Git commit:**

O Git commit irá commitar o arquivo e prepara-lo para o push no repositório do GitHub.

## <span class="underline">Trabalhando com GitHub</span>

Esses comandos serão executados quando o repositório no GitHub já estiver criado.

**Comandos essenciais:**

Comando: **git remote add origin \<link do repositório>** este comando fará com que o apelido \'origin\' se torne o link do repositório.

Comando: **git remote -v** irá verificar se o apelido do comando anterior foi aplicado no link do repositório.

Comando: **git push origin master** irá subir (empurrar) o projeto para o repositório do GitHub**.**

Comando: **git pull origin master** irá puxar o arquivo do servidor remoto para o local, então assim, podendo fazer as correções devidas das duas versões e subir a versão mais atualizada.
