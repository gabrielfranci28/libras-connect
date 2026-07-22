# APIs — Contas e Regras de Uso

## 1. Contas Já Criadas

1. Replit
2. Expo
3. GitHub
4. Firebase
5. LiveKit
6. OpenAI
7. Cloudinary
8. Resend
9. Mercado Pago (Estrutura pronta - chaves serão inseridas posteriormente pelo desenvolvedor)
10. UptimeRobot

## 2. Regra Geral — Nunca Inventar

Nunca inventar:

* API Key
* Secret
* Token
* URL
* Project ID
* Cloud Name
* Client ID
* Client Secret
* App ID
* JSON de credenciais
* Qualquer informação externa

Quando faltar alguma informação, ou for necessário qualquer um dos itens acima, parar imediatamente e perguntar antes de continuar.

## 3. Armazenamento de Credenciais

* Nunca colocar chaves fixas no código (frontend ou backend).
* Usar sempre variáveis de ambiente (Secrets do Replit).
* A chave Pix não deve ficar fixa no código do frontend, apenas no backend.

## 4. Uso de Cada API/Serviço no Projeto

* **Firebase** — banco de dados.
* **Cloudinary** — armazenamento de fotos e vídeos.
* **LiveKit** — videochamada.
* **OpenAI**:
  * Whisper — áudio → texto (usado na legenda automática em vídeo-chamada).
  * GPT-4o — vídeo → texto (usado no tradutor Libras ↔ Português, experimento em beta).
* **Resend** — envio de e-mails (ex.: verificação de e-mail, recuperação de senha).
* **Mercado Pago** — pagamentos via Pix.
* **UptimeRobot** — monitoramento externo do servidor.
* **Expo** — execução e testes do app via Expo Go.
* **GitHub** — controle de versão.
* **Replit** — ambiente de desenvolvimento e hospedagem.

## 5. Rotas Relacionadas a APIs (server.js)

* `app.get('/api/pix-key')` — retorna a chave Pix em formato JSON (somente backend, nunca fixa no frontend).
* `app.get('/ping')` — retorna apenas status 200 OK, para manter o servidor ativo via monitoramento externo (UptimeRobot). Após criar essa rota, informar a URL exata completa a ser usada no UptimeRobot.
