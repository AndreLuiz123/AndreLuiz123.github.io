# AndreLuiz123.github.io

# tp2017-1

### Tutorial Git - Treinamento Profissional

## O que é Git e para que ele serve?

Git é um sistema de controle de versão, ou seja, um sistema que permite o gerenciamento das modificações feitas em um arquivo ou conjunto de arquivos ao longo do tempo.  Esse tipo de ferramenta permite mais organização, velocidade e fluidez no andamento de projetos em equipe, dado que cada participante do projeto faz sua parte independente de seus colegas.

Um sistema de controle de versão funciona baseado em Estações de Trabalho e um Repositório. As estações de trabalho são os locais onde cada membro da equipe trabalha, ao passo que o repositório é onde as modificações feitas no projeto são concentradas.

** O Git se diferencia dos outros Sistemas de controle de versão por dois motivos:**

 *1-Ao contrario de outros Sistemas de Controle de Versão, o Git é do tipo Distribuido:

 *A maioria dos Sistemas de Controle de Versão são do tipo Concentrados. Isso quer dizer que as modificações feitas no projeto são concentradas apenas no repositório e as estações de trabalho só possuem acesso às modificações feitas nelas mesmas. Um Sistema de Controle de Versão Distribuido permite que não só o repositório, mas também as estações de trabalho, tenham acesso a todas as modificações feitas no projeto.*

*2-A forma como se trabalha em um projeto através do Git:*

  *O Git possui três estágios, o Working Directory, a Staging Area e o Git Directory.

   *O Working Directory é o diretório onde se esta trabalhando. Nesse estágio que são feitas as modificações propriamente ditas no projeto.

   *A Staging Area é o "local" onde as modificações feitas no Working Directory ficam antes de serem enviadas para o Repositório. É como se fosse uma sala de espera dessas modificações.

   *O Git Directory é o destino final do projeto, o repositório.

 Ok, agora tendo em mente o motivo de o Git ser importante e como ele funciona, é necessário saber como utiliza-lo. Para isso, vá ao site

  http://git-scm.com

   e clique em "Downloads". Baixe a versão do sistema mais adequada ao seu computador.


 ## Como usar o Git?

O sistema baixado no site http://git-scm.com permite o uso dessa ferramenta através do terminal. Para iniciar o trabalho, abra o git bash(pode ser através do botão direito do mouse, procurando no seu sistema, etc...). Abrindo o git bash, haverá sempre o nome de usuário @ nome da sua máquina, seguido da localização.

 #### exemplo:

 #### fulano@beltrano1cak331 documentos/estudos/git

Para iniciar seu projeto com Git, é necessário primeiro entrar na pasta que você irá trabalhar. Para isso, digite

cd nome da pasta

O git se encaminhará para a referida pasta.

Após isso, através do comando "git init" é criado um repositório na pasta que esta sendo trabalhada para o git, dando inicio ao controle de versão. Essa criação de repositório pode ser confirmada com a pasta .git que aparecerá na localização onde foi digitado "git init".

É interessante notar que, ao lado do "nome de usuário @ nome da sua máquina, seguido da localização" haverá um "(master)"

exemplo:

  fulano@beltrano1cak331 documentos/estudos/git (master)

Isso indica que o estagio no qual se esta é o mais recente do projeto, e não em versões anteriores ou desatualizadas em relação a modificações feitas no projeto.

Após o Git init, para verificar se há alguma mudança no projeto que não foi incluida no repositório da sua máquina, digite "git status".

Se a mudança for interessante, basta digitar "git add nome da pasta modificada", o que fará a mudança feita no arquivo ir para o controle de versão. O git add, em resumo, pega o arquivo que estava no Working Directory e coloca-o na Staging Area.

Já que os arquivos estão na Staging Area, so resta confirmar a entrada deles no Git Directory, ou seja, no repositório. Para isso, basta digitar "git commit -m "Escreve uma mensagem qualquer"".

 ### Quando se deseja saber mais detalhes das modificações nos arquivo do que o git status pode mostrar, existem comando que podem fazer isso:

O "git diff" mostra, através do terminal, as mudanças que ocorreram no Working Directory. Se as mudanças forem para a Staging Area, então elas não serão mostradas pelo git diff.

Caso seja interessante saber como estão das mudanças na Stagin Area, basta digitar "git diff -- staged", mas esse comando não mostra as modificações que estão no Git Directory.

Caso seja interessante saber quais foram os commites enviados ao repositório até o momento, basta digitar "git log".

Se, além dos commites, deseja-se saber quais foram as modificações exatas nos arquivos que estão no Git Directory, basta digitar "git log -p". Esse comando pode ser encarado como uma mistura do "git diff" com o "git log".

Como o "git diff" e o "git log"(juntamente com suas variações) são mostrados pelo terminal, muitas vezes a análise das mudanças nos arquivos através desses comandos torna-se pouco produtiva. Para resolver esse problema, também existe o comando "gitk", que da acesso à interface gráfica do Git. Com essa interface, pode-se analisar todas as mudanças nos arquivos de forma clara e objetiva.

Após terminar o projeto, para enviar o projeto para o github.com(site no qual outros membros da sua equipe podem ver suas modificações), basta, na pagina inicial do github.com, clicar em "new repository" e, após nomea-lo, enviar suas modificações através dos comandos

git remote add origin endereço da página no git
git push -u origin master

#### exemplo:

#### git remote add origin h ttps://github.com/Fulano/projeto-.git
#### git push -u origin master




## Resumindo:

**git init:** Inicia o controle de versão.

**git add:** Coloca modificação dos arquivos na Staging Area.

**git commit:** Coloca arquivos na Staging Area no Working Directory.

**git status:** Verifica se existem modificações no Working Directory ou arquivos no Staging Area para serem commitados.

**git diff:** Mostra, através do terminal, as mudanças feitas nos arquivos do projeto enquanto eles ainda estão no Working Directory.

**git log:** Mostra, através do terminal, todos os commites feitos no projeto.

**git log -p:** Mostra, através do terminal, todos os arquivos commitados e seus commites do projeto.

**gitk:** Mostra, através de uma interface gráfica, as mudanças feitas nos arquivos do projeto.
