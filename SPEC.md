# Especificação Funcional — Libras Connect

## 1. Visão Geral

* Aplicativo para conectar pessoas surdas e ouvintes que sabem Libras.
* Monetização 100% via Pix, sem cartão de crédito.
* Todo o aplicativo em português do Brasil.

## 2. Layout e Comportamento Geral das Telas

### 2.1 Tamanho das Telas

* 100% largura × 100% altura da tela, em qualquer tela do app.
* Sem bordas, sem espaços sobrando, sem ficar pequeno, sem cortar nada.
* Telas de Explorar, Comunidade, Mensagens e Perfil: todas com 100% da largura e 100% da altura disponível.
* Menu sempre embaixo, cabeçalho sempre no topo, encaixado certinho do começo ao fim.

### 2.2 Tema

* Tema padrão: sempre começa em modo branco, mesmo que o celular use tema escuro.
* Modo escuro: só fica disponível para ativar se o usuário quiser, dentro da tela "Perfil".
* Restante do app permanece igual, independente do tema.

### 2.3 Transições entre Abas

* Transições suaves e animadas ao trocar de uma aba para outra.
* O conteúdo deve deslizar ou aparecer suavemente (efeito de deslizamento horizontal/vertical ou aparecimento gradual).
* A transição deve ser fluida e natural, sem cortes bruscos ou travamentos.
* Tecnologia visual preferencial: CSS (transition/animation) ou recursos nativos do React Native.

### 2.4 Regra Geral de Funcionamento

* Tudo deve funcionar de verdade, não pode ficar parado como desenho.
* Nenhum botão pode ficar sem resposta ao ser pressionado.

## 3. Cadastro / "Conte sobre você"

* Adicionar dois campos novos, logo abaixo do título "Conte sobre você", antes de "Nome completo":
  1. **E-mail\*** — placeholder: "seuemail@exemplo.com" — regra: o e-mail deve ser verificado.
  2. **Senha\*** — placeholder: "Crie uma senha segura" — com botão de ver/ocultar senha.
* Adicionar o texto "Política de Privacidade" onde for necessário.

## 4. Perfil

### 4.1 Álbuns

* Seção ÁLBUNS logo abaixo de "LOCALIZAÇÃO".
* Espaço para 6 álbuns/fotos.
* Botão: "+ Adicionar".
* Ao abrir fotos dos álbuns, existem botões "< anterior" e "> próximo".

### 4.2 Visualização de Fotos (perfil, álbuns e mensagens)

* Ao apertar em qualquer foto de perfil, álbuns ou foto enviada em mensagem, ela abre com:
  1. **Zoom** — deve funcionar: pode aumentar e diminuir a imagem.
  2. **Baixar** — deve funcionar: pode salvar a imagem no celular.
  3. **Denunciar** — deve funcionar: botão para avisar quando houver nudez ou conteúdo errado (a verificação de nudez é feita via denúncia dos usuários, para a moderação analisar).

### 4.3 Amigos

* **Quem pode ver:** 
  * O próprio usuário pode ver a sua lista e quantidade de amigos no seu perfil.
  * Outros usuários que visitarem o perfil também podem ver essa quantidade/lista de amigos.

* **Exibição na tela:**
  * **Com amigos:** Quando a "Solicitação enviada" for aceita, deve exibir o ícone de perfil e a quantidade de amigos (exemplo: **👥 1 amigo**).
  * **Sem amigos:** Se o usuário não tiver nenhum amigo, deve exibir o texto: **"Nenhum amigo"**.

* **Opções da Lista de Amigos (Menu de 3 pontos):**
  * Ao lado de cada amigo na lista, deve existir um botão de **3 pontos (...)** com as opções:
    1. **Excluir amigo:** Remove a pessoa da lista de amizades.
    2. **Bloquear:** Impede a pessoa de ver o perfil, enviar mensagens ou novas solicitações.
    3. **Denunciar:** Abre a opção para reportar o perfil para a moderação analisar.

### 4.4 Favorito

* Opção "Favorito" disponível no perfil.
* Ao apertar nela, aparece um espaço para escrever, que pode estar vazio.

### 4.5 Acesso à tela de Pagamentos

* Ao clicar (dentro do Perfil), abre a tela completa dos pagamentos (ver seção 12).

### 4.6 Acesso à tela de Privacidade

* Ao clicar (dentro do Perfil), abre a tela inteira das configurações de Privacidade (ver seção 10).

## 5. Solicitar conexão / Início de Conversa

* Botão "Solicitar conexão": remover somente o ícone/desenho, mantendo o texto do botão.
* Remover:
  1. Botão "Ver perfil completo e fotos".
  2. Etiqueta "Surdo" que fica acima.
  3. Ícone de imagem que fica à esquerda do campo de mensagem.
* Organizar assim:
  1. Manter apenas o texto: "Diga olá e inicie uma conversa".
  2. No lugar do ícone de imagem, colocar o ícone de anexar — ao apertar, abre opções de verdade: foto, vídeo, localização, arquivos e mais. Cada opção deve funcionar quando escolhida.
  3. Fotos e vídeos: usar aspectRatio 1080/1350 com resizeMode "contain" — não usar tamanho fixo em pixels. Isso garante que a imagem apareça inteira em qualquer tamanho de tela, sem cortar, esticar ou diminuir.
  4. Vídeos seguem a mesma regra: exibição completa, com baixar, denunciar, ocultar e desfazer ocultar funcionais.

## 6. Comunidade (antes chamada "Conexões")

* Trocar "Conexões" para "Comunidade".
* Ao publicar algo, aparece a pergunta: "O que você gostaria de colocar?".
* Os usuários podem compartilhar:
  * Fotos e vídeos para ensinar Libras.
  * Eventos da comunidade.
  * Aulas pagas ou gratuitas.
  * Direitos de acessibilidade.
  * Criação de grupos.
  * Publicações apenas de texto.
* Interações nas publicações: desenhos de "Joinha" e "Não joinha", opção de comentar, desenho de favorito, possibilidade de escrever legenda abaixo da foto ou vídeo.
* Todas as fotos, vídeos e textos publicados sempre têm um menu de 3 pontos.
* **Para o próprio autor do post:** exibe as opções **Editar** (permite editar a legenda/texto) e **Excluir** (exibe confirmação antes de apagar).
  * **Para outros usuários:** exibe as opções **Denunciar** e **Bloquear**.
* Se alguém ensina sinais para enganar ou aplicar golpes e recebe denúncias, o conteúdo é removido.
* **Publicação de Mídias e Detecção Automática (18+):**
  * Quando um usuário publicar uma foto ou vídeo contendo mídia sensível (18+), o sistema/IA deve detectar e aplicar automaticamente a tag de Mídia Sensível (censura borrada).
  * Por padrão, a publicação aparece borrada com o botão "Clique para ver".
  * Ela só será exibida diretamente e sem borrão para os usuários que alterarem a opção em Privacidade para "Sem censura".

### 6.4 Direitos de Acessibilidade

* Ao apertar em "Direitos de acessibilidade", abre uma tela de soluções com:
  * **Guia de Direitos:** Informações claras sobre leis de acessibilidade e Libras.
  * **Modelos Prontos:** Opção para gerar/baixar pedidos formais de intérprete para hospitais, faculdades ou órgãos públicos.
  * **Onde Buscar Ajuda:** Orientações e canais para denunciar falta de acessibilidade. 
* **Vídeos com Intérprete de Libras:** Conteúdos em vídeo gratuitos com tradução em Libras para explicar direitos e soluções.
  * **Apoio da Comunidade:** Intérpretes voluntários podem colaborar gravando vídeos, com opção de receber apoio/gorjeta voluntária dos usuários.

### 6.1 Criar Grupos

* Ao apertar em "Criar grupos", aparece a pergunta: "O que você busca?".
* Abaixo, um campo para escrever (vazio ou preenchido).
* Ao lado, os itens: nome do grupo, quantidade de pessoas, opção de escolher se o grupo será aberto ou privado. 
* **Visualização de Membros:** 
    * Em grupos **abertos**, qualquer usuário pode visualizar a lista de membros do grupo.
    * Em grupos **privados**, apenas os membros participantes podem ver a lista de quem está no grupo.

### 6.2 Eventos da Comunidade

* Ao apertar em Eventos da comunidade, abre e mostra a lista com local, data e tipo de evento — como festas, encontros, reuniões e atividades em geral.

### 6.3 Aulas Pagas ou Gratuitas

* Ao apertar em "Aulas pagas ou gratuitas", se o usuário for fluente, ele pode criar sua própria página de aulas, definindo nome da página, valor e demais informações.
* **Segurança e Proteção contra Golpes:**
  * **Sistema de Avaliação:** Alunos podem avaliar a aula com notas (1 a 5 estrelas) e comentários.
  * **Garantia de Pagamento:** O pagamento das aulas pagas fica retido na plataforma até a conclusão do serviço para proteger o aluno contra golpes.
  * **Denúncia de Conteúdo Falso:** Botão para denunciar aulas que ensinem sinais incorretos com intenção de enganar ou que apliquem golpes. Caso comprovado, o valor é reembolsado ao aluno e a página é suspensa.
* Campo de busca com a pergunta: "O que você gostaria de buscar?".

## 7. Mensagens / Chat

### 7.1 Comportamento da Conversa

* As mensagens aparecem na área de conversa crescendo para baixo — cada nova mensagem é adicionada embaixo das anteriores, bem perto do campo "Escreva uma mensagem...".
* Não deve rolar automaticamente para o topo; o foco deve ficar sempre próximo ao campo de entrada, como no Telegram ou WhatsApp.

### 7.2 Envio de Mensagem

* Quando o usuário apertar "Enviar", a mensagem não deve aparecer instantaneamente.
* Deve ter um pequeno atraso ou animação suave (ex.: a bolha "voa" ou desce devagar até o lugar), para não ficar rápido e artificial — parecendo natural, como se a mensagem estivesse sendo "colocada" na conversa.

### 7.3 Indicador de Status (offline)

* Quando sem internet, as mensagens ficam em fila local e enviam automaticamente quando a conexão voltar.
* Indicador visual: "Enviando..." → "Enviado" → "Lido".

### 7.4 Ações do Chat

* Bloquear, Denunciar, Limpar a conversa.
* Devem funcionar quando apertadas: abrir confirmação e executar a ação. Não podem ficar paradas sem resposta.

### 7.5 Chat com Perfil Bloqueado

* Quando alguém bloquear o perfil de outra pessoa, a página é desenhada como bloqueada, mostrando os avisos: "Você bloqueou" ou "Ele(a) te bloqueou".
* O campo "Escreva uma mensagem..." também é desenhado com essa indicação de bloqueio.

### 7.6 Chat com Perfil Bloqueado por Denúncias

* Se o perfil foi bloqueado por receber denúncias, a página mostra o desenho de aviso de denúncia, com o texto: "Este perfil foi bloqueado por denúncias".
* O campo "Escreva uma mensagem..." some.

### 7.7 Chat com Perfil Excluído

* Se o próprio usuário excluiu a conta, a página mostra o desenho de exclusão, com o texto: "Este perfil foi excluído pelo próprio usuário".
* O campo "Escreva uma mensagem..." some.

### 7.8 Indicador de Mensagem Nova

* Bolinha pequena vermelha ao lado do botão "Mensagens" quando houver mensagem nova ou não lida.

### 7.9 Gestão da Lista de Conversas (Tocar e Segurar)

* Ao tocar e segurar (toque longo) sobre qualquer conversa na lista de mensagens, abre um menu de opções rápidas:
  * **Fixar conversa:** Fixa o chat no topo da lista.
  * **Silenciar notificações:** Opções de tempo (ex.: 8 horas, 1 semana) ou permanentemente.
  * **Apagar conversa:** Ao clicar nesta opção, exibe janela de confirmação: *"Tem certeza que deseja apagar esta conversa?"* com os botões **Apagar** e **Cancelar**.

## 8. Vídeo-chamada

* Quando um usuário iniciar uma chamada de vídeo, é exibida uma opção para aceitar ou recusar.
* Quando alguém recusar, avisar: "Ele(a) recusou".

## 9. Notificações

* **Avisos de amizade:** Notifica quando o usuário recebe uma solicitação ou quando uma "Solicitação enviada" é aceita por outra pessoa.
* **Aba Notificações:** Exibe a lista de atualizações e confirmações de novas amizades.
* **Interações:** Quando alguém der "Joinha", "Não joinha", comentar ou favoritar, o usuário recebe uma pequena bolinha vermelha de notificação no ícone.
* **Grupos:** Na criação de grupos (com nome, quantidade de pessoas, aberto ou privado), quando um administrador aprovar ou recusar a entrada de alguém, o usuário recebe uma notificação avisando o resultado.

## 10. Privacidade

* Ao clicar (dentro do Perfil), abre a tela inteira das configurações de Privacidade.
* Opções configuráveis (Público, Amigos, Somente eu):
  1. Quem pode ver sua lista de amigos.
  2. Privatização do Perfil: Perfil Público ou Perfil Privado.
  3. Quem pode entrar no seu perfil.
  4. Quem pode te enviar mensagem.
  5. Quem pode te enviar uma foto na mensagem.
  6. Quem pode te enviar um vídeo na mensagem.
  7. Quem pode te chamar de vídeo.
* **Filtro de Conteúdo Sensível (18+):**
  * Funcionalidade restrita exclusivamente para contas verificadas como maiores de 18 anos.
  * Opção configurável pelo usuário: **"Com censura (borrado)"** ou **"Sem censura"**.
  * **Padrão:** Mídias sensíveis vêm borradas com o botão "Clique para ver".
  * Se o usuário escolher "Sem censura", as mídias autorizadas para sua faixa etária serão exibidas diretamente.
* **Confirmação ao Sair (Prevenção de Perda de Alterações):**
  * Se o usuário alterar qualquer configuração e tentar sair da tela sem clicar em **"Aplicar"**, o aplicativo deve exibir um aviso:
  * **Mensagem:** *"Você possui alterações não salvas. Tem certeza que deseja sair sem aplicar?"*
  * **Opções dos botões:** **"Sair sem aplicar"** e **"Continuar editando"**.
* Tudo deve funcionar de verdade.
* Se escolher a opção "Bloquear" para chamada de vídeo, quando alguém tentar te chamar, aparece o aviso: "Esta opção está bloqueada".
* Quando alguém tentar acessar um perfil com a opção de bloqueio ativada, a tela aparece desenhada como perfil privado.
* Quando o perfil aceitar a solicitação de amizade, ele fica aberto apenas para Amigos.

# 11. Configurações

Ao clicar em **Configurações** (dentro do Perfil), abre a tela principal de ajustes do aplicativo:

* **Aparência / Tema:** Alternar entre **Modo Escuro** (Dark Mode) e **Modo Claro** (Light Mode), ou seguir o Padrão do Sistema.
* **Notificações:** Ativar ou desativar alertas de mensagens, solicitações de amizade, eventos e avisos do grupo.
* **Sons do Aplicativo:** Ativar ou desativar os sons de envio de mensagem, cliques e notificações.
* **Acessibilidade de Texto:** Ajustar o tamanho da fonte (texto normal, grande ou extra grande) para facilitar a leitura.

## 12. Moderação e Denúncias

* Em todos os perfis, o menu de 3 pontos apresenta as opções Bloquear e Denunciar.
* Ao confirmar uma denúncia, a moderação analisa com cuidado e remove apenas conteúdos ilegais ou não autorizados. Conteúdos 18+ com o filtro de censura ativado (postados por adultos verificados) são permitidos e não serão removidos.
* Se verificar que o perfil realmente cometeu infrações e recebeu 5 denúncias válidas, ele será excluído permanentemente.
* Regra de segurança do chat: se alguém enviar mensagens com falta de respeito ou conteúdo proibido, e receber 5 denúncias reais validadas por moderação humana, a conta será excluída permanentemente.
* Tudo deve funcionar corretamente, sem travar.

## 13. Pagamentos (Monetização via Pix)

### 12.1 Regra Geral (aplica-se a todos os recursos pagos)

* Todo conteúdo pago fica coberto por fundo escuro/transparente até o pagamento ser confirmado.
* Embaixo do bloqueio, botão escrito: "Pagar".
* Abaixo do botão, texto fixo: "Pagamento só via Pix para Libras Connect".
* Quando o Pix é confirmado, libera o acesso automaticamente (isso exigirá integração com API de pagamento real no futuro).

### 12.2 Pacote Tudo Liberado

* Exibido no topo de todas as telas de pagamento.
* Valor: R$ 38,00.
* No pacote, o usuário paga o mesmo valor e tem TUDO liberado por 2 meses inteiros, sem precisar comprar um por um.
* Até pagar o pacote, todos os itens individuais ficam bloqueados.

### 12.3 Recursos Individuais (caso não queira o pacote)

1. Destaque no topo das buscas — R$ 3,00 por 7 dias.
2. Badge verificado dourado "Perfil real Libras Connect" — R$ 10,00 vitalício.
3. Legenda automática em vídeo-chamada — R$ 4,00 por chamada. Transforma a fala do ouvinte em texto grande na tela em tempo real, usando Whisper/OpenAI.
4. Tradutor Libras ↔ Português por IA (experimento em beta) — R$ 6,00/mês. O vídeo de sinal vira texto, usando GPT-4o. Incluir aviso na interface: "Funciona como experimento, pode conter erros na tradução."
5. Aviso de som ambiente — R$ 5,00/mês. Detecta campainha, batida na porta, choro de bebê; avisa com vibração forte. Incluir aviso na interface: "Funciona como apoio, não substitui sistemas profissionais de alerta." Começar com 2 a 3 sons apenas.
6. Gravar chamada de vídeo em Libras — R$ 3,00 por gravação. Salva o vídeo em alta qualidade por 7 dias e gera link privado.
7. Desbloquear álbum de vídeos em Libras de outra pessoa — R$ 4,00 por álbum.
8. Verificação de foto real por IA — R$ 3,00 vitalício.

## 14. Inteligência Artificial (OpenAI)

* Whisper: áudio → texto.
* GPT-4o: vídeo → texto.
* Atenção: a função de tradução (Libras ↔ Português) é um experimento em beta e pode conter erros. O app deve exibir na tela do usuário o aviso: "Funciona como experimento, pode conter erros na tradução."

## 15. Regras Técnicas Gerais

* Banco de dados simples para usuários, pagamentos e logs.
* Fotos e vídeos armazenados em Cloudinary.
* Chat em tempo real com Socket.io + Node.js.
* Tratamento offline: quando sem internet, mensagens ficam em fila local e enviam automaticamente quando a conexão voltar.
* Limite de tamanho de arquivo: fotos máximo 10MB, vídeos máximo 50MB.
* Fluxo de recuperação de senha via e-mail com código de verificação.
