# Estrutura do Projeto

## 1. Tecnologias

* Frontend: Expo + React Native
* Backend: Node.js + Express
* Chat em tempo real: Socket.io
* Armazenamento de mídia: Cloudinary

## 2. Arquivos Base do Projeto

* package.json
* app.json
* App.js
* server.js

## 3. Configuração do Expo

1. package.json compatível com Expo, com o comando de inicialização ("start") configurado para iniciar o servidor do Expo (`expo start`).
2. Configurar o túnel de conexão do Expo (parâmetro `--tunnel`) para permitir a leitura do QR Code gerado pelo Replit usando a câmera do celular através do Expo Go.
3. Usar o comando `expo start --tunnel` para que o QR Code possa ser lido pelo celular via Expo Go.
4. Garantir que as permissões nativas do Expo estejam declaradas no app.json: vibration, camera, microphone.
5. Criar uma estrutura simples com uma tela inicial em App.js ocupando 100% da tela, para iniciar o desenvolvimento visual.

## 4. Layout Geral das Telas

* 100% largura × 100% altura da tela, em qualquer tela do app — sem bordas, sem espaços sobrando, sem ficar pequeno, sem cortar nada.
* Telas de Explorar, Comunidade, Mensagens e Perfil: todas com 100% da largura e 100% da altura disponível.
* Menu sempre embaixo, cabeçalho sempre no topo, encaixado certinho do começo ao fim.

## 5. Tema

* Tema padrão: sempre começa em modo branco (claro), mesmo que o celular esteja em tema escuro.
* Modo escuro: disponível apenas se ativado pelo usuário, dentro da tela "Perfil".
* Restante do app permanece igual, independente do tema.

## 6. Transições entre Abas

* Transições suaves e animadas ao trocar de aba.
* O conteúdo deve deslizar ou aparecer suavemente (efeito de deslizamento horizontal/vertical ou aparecimento gradual).
* A transição deve ser fluida e natural, sem cortes bruscos ou travamentos.
* Tecnologia visual preferencial: CSS (transition/animation) ou recursos nativos do React Native.

## 7. Exibição de Fotos e Vídeos

* Usar aspectRatio 1080/1350 com resizeMode "contain" — não usar tamanho fixo em pixels.
* Isso garante que a imagem/vídeo apareça inteiro em qualquer tamanho de tela, sem cortar, esticar ou diminuir.
