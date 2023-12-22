# gitflowtop

Alteração feita direto no GITHUB.

Segunda alteração feita direto no GITHUB.

Terceira alteração feita direto no GITHUB.

Para sempre manter o projeto atualizado com o projeto original:

Primeiramente fizemos uma alteração na conta principal (passando por cima das regras e criando direto no main)
Alteração simples dentro do readme.

Quando fazemos um git pull no secundário não vemos essa alteração. E mostra no github que estamos 1 commit atrás do original
Temos duas opções:

Primeira é diretamente no site do github, clicar na opção atualizar o fork, assim fazemos o git pull e estará atualizado.

Segunda forma é adicionando um novo repositório remoto chamado upstream com o repositório original
git remote add upstream https://github.com/vanderleipinto/gitflowtop
Agora temos referência aos dois repositórios.
Se fizermos um git pull ele vai direto no origin e não atualiza com o principal.
Para atualizarmos com o projeto original usando pull e o upstream faremos:

git pull upstream main

Onde main é a branch que faremos o pull

OBS: Desta maneira só é atualizado o repositório da conta secundária no local e não no remoto.

Uma vez atualizado o repositório local com o original, podemos fazer um git push origin main para atualizar o repositório secundário remoto.

BRANCHES PRINCIPAIS ---------------------------------

Base geral de branches principais.
No repositório local temos a branch main que é a principal. Ultima versão pública e disponível.

Como o repositório principal não aceita alterações na branch principal, criaremos (no repositório local) outra branch que será responsável pelas mudanças (DEVELOP ou DEV ou DEVELOPMENT)

Agora criaremos novas branchs para novas funcionalidades a partir de DEV.

CRIANDO A BRANCH DEV
git branch develop

Agora para criar novas funcionalidades criaremos mais uma branch para tal. Uma vez terminada e testada a funcionalidade faremos um merge para a branch develop e apagamos essa branch da funcionalidade adicionada.

Quando terminadas todas as funcionalidades em DEV, criaremos uma nova branch chamada RELEASE que será enviada para o remoto e do remoto será criado um pull request para mandar para o main do original.
