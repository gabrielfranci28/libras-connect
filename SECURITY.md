# Segurança, Privacidade e Moderação

## 1. Regras de Credenciais

* Nunca inventar API Key, Secret, Token, URL, Project ID, Cloud Name, Client ID, Client Secret, App ID ou JSON de credenciais.
* Quando faltar alguma informação, parar e perguntar antes de continuar.
* Nunca colocar chaves fixas no código.
* Usar sempre variáveis de ambiente (Secrets do Replit).
* A chave Pix nunca deve ficar fixa no frontend, apenas no backend (rota `/api/pix-key`).

## 2. Bloqueio entre Usuários

* Ações "Bloquear", "Denunciar" e "Limpar a conversa" disponíveis no chat — devem funcionar de verdade: ao apertar, abrir confirmação e executar a ação.
* Quando alguém bloqueia o perfil de outra pessoa, a página é exibida como bloqueada, mostrando os avisos: "Você bloqueou" ou "Ele(a) te bloqueou".
* O campo "Escreva uma mensagem..." também é exibido com indicação de bloqueio.

## 3. Denúncias e Moderação

* Em todos os perfis, o menu de 3 pontos apresenta as opções Bloquear e Denunciar.
* Ao confirmar uma denúncia, a moderação analisa com cuidado e remove apenas o conteúdo ou a conta de forma justa, sem injustiças.
* Se o perfil realmente cometeu infrações e recebeu 5 denúncias válidas, ele é excluído permanentemente.
* Regra de segurança do chat: se alguém enviar mensagens com falta de respeito ou conteúdo proibido e receber 5 denúncias reais validadas por moderação humana, a conta será excluída permanentemente.
* Se alguém ensina sinais para enganar ou aplicar golpes na Comunidade e recebe denúncias, o conteúdo é removido.
* A plataforma deve proteger todo o conteúdo e todos os usuários.
* A verificação de nudez em fotos é feita via denúncia dos usuários, analisada pela moderação (botão "Denunciar" disponível ao visualizar fotos de perfil, álbuns ou mensagens).
* Tudo deve funcionar corretamente, sem travar.

## 4. Estados de Perfil

* **Perfil bloqueado por denúncias**: exibir o desenho de aviso de denúncia com o texto "Este perfil foi bloqueado por denúncias"; o campo "Escreva uma mensagem..." some.
* **Perfil excluído pelo próprio usuário**: exibir o desenho de exclusão com o texto "Este perfil foi excluído pelo próprio usuário"; o campo "Escreva uma mensagem..." some.

## 5. Recursos de Segurança/Verificação Pagos

* Badge verificado dourado "Perfil real Libras Connect" — R$ 10,00 vitalício.
* Verificação de foto real por IA — R$ 3,00 vitalício.

## 6. Avisos Obrigatórios na Interface

* Tradutor Libras ↔ Português por IA (beta): "Funciona como experimento, pode conter erros na tradução."
* Aviso de som ambiente: "Funciona como apoio, não substitui sistemas profissionais de alerta."
* Texto "Política de Privacidade" adicionado onde for necessário.
