# Deploy e Execução

## 1. Ambiente de Desenvolvimento

* Replit como ambiente de desenvolvimento/hospedagem.
* GitHub para controle de versão.

## 2. Execução via Expo Go

1. package.json compatível com Expo, com o comando "start" configurado para iniciar o servidor do Expo (`expo start`).
2. Configurar o túnel de conexão do Expo (parâmetro `--tunnel`).
3. Usar o comando `expo start --tunnel` para que o QR Code gerado pelo Replit possa ser lido pela câmera do celular através do Expo Go.
4. O aplicativo deve funcionar completamente no Expo Go.

## 3. Permissões Nativas (app.json)

* vibration
* camera
* microphone

## 4. Monitoramento (UptimeRobot)

* Criar no server.js a rota `app.get('/ping')`, que retorna apenas status 200 OK, para manter o servidor ativo via monitoramento externo.
* Após criar essa rota, informar a URL exata completa a ser copiada e colada no UptimeRobot.

## 5. Variáveis de Ambiente / Secrets

* Todas as chaves, tokens e credenciais devem ser configuradas como variáveis de ambiente (Secrets do Replit).
* Nenhuma chave deve ficar fixa no código.
