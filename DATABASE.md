# Banco de Dados e Armazenamento

## 1. Banco de Dados

* Banco de dados simples para: usuários, pagamentos e logs.
* Serviço utilizado: Firebase.

## 2. Armazenamento de Mídia

* Fotos e vídeos armazenados em Cloudinary.

## 3. Limites de Arquivo

* Fotos: máximo 10MB.
* Vídeos: máximo 50MB.

## 4. Mensagens (Chat)

* Chat em tempo real com Socket.io + Node.js.
* Tratamento offline: quando sem internet, mensagens ficam em fila local e enviam automaticamente quando a conexão voltar.
* Indicador visual de status da mensagem: "Enviando..." → "Enviado" → "Lido".

## 5. Autenticação e Recuperação de Senha

* Fluxo de recuperação de senha via e-mail com código de verificação (Resend).
* O e-mail cadastrado deve ser verificado.

## 6. Pix

* Rota `app.get('/api/pix-key')` no server.js retorna a chave Pix em formato JSON.
* A chave Pix não deve ficar fixa no código do frontend, apenas no backend.
