# Notas de atualização
Colocarei neste arquivos as mudanças significativas em cada versão começando na versão 3.0.0

## 3.1.5 - 04/04/2025

### CORREÇÕES
- Correção na escolha de método de autenticação no Termux

## 3.1.4 - 04/04/2025

### GERAL
- Adicionado suporte a código de pareamento, quando iniciar o bot pela primeira vez será perguntado se deseja se conectar pelo QR Code ou Código de pareamento.
- Removida a necessidade de configurar API Key para funcionamento de certos comandos.
- Erros de chamadas externas de API/Bibliotecas agoras são exibidas no console.
- Novo recurso de grupo para **filtrar palavras e deletar mensagem** se alguma palavra do filtro for detectada.

### COMANDOS
- Novo comando de admin **!modoadmin** para apenas administradores do bot conseguirem usar comandos.
- Novo comando de grupo **!rmaviso** para remover aviso de um membro.
- Novo comando de grupo **!zeraravisos** para zerar os avisos de todos os membros.
- Novo comando de grupo **!addfiltros** para adicionar palavras ao filtro do grupo.
- Novo comando de grupo **!rmfiltros** para remover palavas do filtro do grupo.
- Comando **!grupo** agora também exibe os filtros de palavras ativos no grupo.
- Suporte ao campeonato de 2025 no comando **!brasileirao**.

### CORREÇÕES
- Correção na reprodução do video no comando **!qualanime**


## 3.1.3 - 31/03/2025

### COMANDOS
- Comando **!ia** foi adicionado novamente
- Comando **!criarimg** foi adicionado novamente

### CORREÇÕES
- Correção na mensagem de espera do comando **!play**
- Correção no problema de download dos comandos **!play** e **!yt**
- Correção no antiflood que ficava sempre ativo mesmo ele estando desativado.


## 3.1.2 - 29/03/2025

### CORREÇÕES
- Corrigida a sincronização inicial de grupos e da lista negra
- Corrigida resposta quando não encontra nenhuma letra de música pelo comando **!letra**


## 3.1.1 - 28/03/2025

### CORREÇÕES
- Corrigida a atualização de grupos quando o bot inicia, agora ele remove corretamente os participantes do banco de dados que já sairam do grupo.
- Corrigido banimento do comando **!aviso**, agora ao chegar aos 3 avisos ele irá banir corretamente e adicionar a lista negra.


## 3.1.0 - 28/03/2025

### GERAL
- Reorganização na estrutura do projeto para me facilitar na manutenção.
- O atualizador agora verifica se a versão nova é compativel com os dados atuais, caso não seja será perguntado se deseja instalar a versão nova e deletar os dados antigos.
- Implementação de banco de dados para guardar os dados de participantes dos grupos.

### COMANDOS
- Comando **!menu** agora não exibe a categoria grupo quando é usado no privado.
- Comando **!contador** foi removido e agora o contador já está integrado com o grupo.
- Comando **!atividade** foi renomeado para **!membro** e foram adicionadas informações adicionais sobre o membro do grupo.
- Comando **!verusuario** foi renomeado para **!usuario**
- Comando **!veradmins** foi renomeado para **!admins**
- Comando **!vergrupos** foi renomeado para **!grupos**
- Novo comando de grupo **!aviso** (Se o membro receber 3 avisos será automaticamente adicionado a lista negra).

### CORREÇÕES
- Corrigida a resposta do comando **!par**
- Modificado visual do menu para corrigir o visual quebrado em alguns navegadores no PC.
- Corrigida falha que se o usuário fosse bloqueado pelo bot ele não passava pelos filtros dos recursos de segurança do grupo.


## 3.0.2 - 24/03/2025

### GERAL
- Agora quando uma atualização é feita a pasta da versão anterior é deletada para evitar os arquivos que não são mais usados se acumulem.
- Projeto foi reorganizado e agora as API's estão juntas com o bot para facilitar nas atualizações.

### COMANDOS
- Novo comando **!steamverde** para procurar links de "jogos alternativos" para PC.
- Comando **!simi** removido do bot.

### CORREÇÕES
- Os comandos **!ouvir** e **!qualmusica** foram corrigidos e agora recebem a chave de API corretamente.

## 3.0.1 - 21/03/2025

### NOVO
- Novos comandos **!sorteio** para sortear um número.
- Novo comando **!sorteiomembro** para sortear um membro do grupo.

### MUDANÇAS
- O comando **!roletarussa** foi reescrito para ficar mais fiel ao jogo real e agora funciona também em chat privado.

### CORREÇÕES
- Agora se o atualizador não se conseguir se conectar ao GitHub ele não irá impedir de inicializar o bot.

## 3.0.0 - 21/03/2025

### GERAL
- O projeto foi totalmente reescrito para Typescript.
- Agora o projeto utiliza a [**biblioteca-lbot**](https://www.npmjs.com/package/@victorsouzaleal/biblioteca-lbot) para obter dados externos para os comandos.
- Adicionada verificação de versão ao iniciar e se for possível ele fará a atualização automaticamente.
- O visual dos menus e das mensagens de resposta foram reformulados.
- Adicionado suporte a chats que tem mensagens temporárias que desaparecem com o tempo.
- Adicionado recurso de **múltiplos administradores do bot**.
- A configuração de chaves de API agora é feita por comando.
- O recurso de grupo **contador** foi reescrito
- O recurso **Taxa de comandos** foi reescrito
- O recurso **Anti-flood** foi reescrito 
- Os recursos de **Limite diário de comandos** e de **Tipo de usuário** foram removidos.
- O recurso de **Revelar mensagens de visualização única** foi removido.
- Melhoria na fila de eventos em espera enquanto o bot inicializa.
- Melhoria no tratamento de erro nos comandos para o usuário saber o que houve de errado.
- Melhoria no armazenamento de mensagens do bot.
- Melhorias em geral em comandos.
- A categoria de comando **DIVERSÃO** foi renomeada para **VARIADO**


### COMANDOS 

#### Mudanças
- Melhoria nos comandos da categoria DOWNLOAD dando mais informações sobre a mídia baixada e agora permite downloads de no máximo **6 MINUTOS**.
- Melhorias nos comandos da categoria VARIADO, alguns comandos foram reescritos.
- Comando **!s** agora possibilita fazer sticker sem redimensionar a imagem original usando o comando **!s 2**.
- Comando **!status** foi renomeado para **!grupo** e agora exibe mais informações sobre o grupo inclusive quantos comandos foram feitos e quais recursos estão ativos/desativados.
- Comando **!info** agora exibe o contatos de todos que estão registrados como administrador do bot.
- Comando **!reportar** agora reporta a mensagem para todos que estão registrados como administrador do bot.
- Comando **!remlista** foi renomeado para **!rmlista** e agora não é mais necessário digitar o número completo da pessoa que você quer remover da lista negra, é só usar o **!listanegra** e ver qual posição da lista a pessoa que você quer remover está e usar o rmlista. Por exemplo **!rmlista 1** remove a pessoa da posição 1 da lista negra.
- Comando **!listanegra** agora exibe quantos usuários estão na lista negra, e se o usuário que está na lista já tiver tido contato com o bot também será exibido o nome dele ao lado do número.
- Comando **!tw** foi renomeado para **!x**
- Comando **!nomeadm** foi renomeado para **!nomeautor** e agora serve para renomear o nome do autor das figurinhas.
- Comando **!nomesticker** foi renomeado para **!nomepack** e agora serve para renomear o nome do pack das figurinhas.
- Comando **!alink** foi renomeado para **!antilink**.
- Comando **!afake** foi renomeado para **!antifake**.
- Comando **!aflood** foi renomeado para **!antiflood**.
- Comando **!bv** foi renomeado para **!bemvindo**.
- Comando **!fch** foi renomeado para **!frase**.
- Comando **!add** teve a resposta melhorada e só adiciona 1 membro pro comando ao grupo para evitar banimentos.
- Comando **!ban** teve a resposta melhorada e exibe se conseguiu banir ou não o participante.
- Todos os comandos de marcação **!mm**, **!mt** e **!adms** agora usam marcação silenciosa para evitar mostrar uma lista muito grande de pessoas marcadas.
- Comando **!topativos** como padrão agora exibe o ranking dos 10 membros com mais mensagens no grupo.
- Comando **imarcar** foi renomeado para **!inativos**.
- Comando **!verdados** foi renomeado para **!verusuario**
- Comando **!grupos** foi renomeado para **!vergrupos**
- Comando **!estado** foi renomeado para **!recado** e agora pode ser usado para colocar qualquer texto na parte de recado/status no perfil do bot.
- Os comandos **!sair** , **!linkgrupo** e **!sairgrupos** não ficarão mais expostos no menu de admin, eles serão subcomandos do comando **!vergrupos**.
- Comando **!pvliberado** foi renomeado para **!comandospv**
- Comando **!info** agora exibe quais recursos do bot estão ligados/desligados se quem fizer o comando for administrador do bot.

#### Novo
- Novos comandos **!addadmin**, **!rmadmin**, **!veradmins** para adicionar, remover e listar os administradores do bot.
- Novo comando **!api** para configurar as chaves de API sem a necessidade de alterar o .env.

#### Removidos
- Comandos de limite diário e de tipos de usuários **!limitediario**, **!usuarios**, **!tipos**, **!novotipo**, **!tipotitulo**, **!deltipo**, **!usuariotipo**, **!limpartipo**, **!tipocomandos**, **!rtodos**, **!r** foram removidos.
- Comandos de revelar mensagens **!autorevelar** e **!revelar** foram removidos.
- Comando **!rt** foi removido.
- Comando **!enquete** foi removido.
- Comando **!regras** foi removido e foi integrado ao **!grupo**
- Comando **!rastreio** foi removido por não ter mais suporte dos Correios.
- Comandos **!ia** e **!criarimg** removidos, e serão adicionados novamente se voltarem a funcionar ou eu achar alguma alternativa gratuita.
- Comando **!bantodos** foi removido.
- Comando **ibanir** foi removido.
- Comando **!infobot** foi removido, o comando **!info** vai servir para a função dele.




