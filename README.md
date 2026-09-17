# Conecta Online

Versão completa de mensageiro com login, chat em tempo real e envio de mídia.

## Recursos
- Cadastro/login.
- Conversas privadas e WebSocket.
- Mensagens persistentes.
- Fotos, vídeos, áudios e documentos.
- Gravação de áudio pelo navegador.
- Interface responsiva para celular.
- Upload limitado a 60 MB por arquivo.

## Rodar localmente
Requer Node.js 18+:

```bash
npm install
npm start
```

Abra `http://localhost:3000`. Para testar entre duas pessoas, crie dois usuários em navegadores diferentes.

## Colocar online
Hospede em um serviço Node.js com HTTPS e armazenamento persistente. Para produção, troque o JSON local por um banco e os uploads locais por armazenamento de objetos (S3, Cloud Storage etc.). Configure backup, limites, política de privacidade e criptografia antes de abrir para público.

## Publicar no Render

1. Crie um repositório no GitHub e envie todos os arquivos desta pasta.
2. No Render, escolha **New > Web Service** e conecte o repositório.
3. Use `npm install` no Build Command e `npm start` no Start Command.
4. O arquivo `render.yaml` já contém a configuração básica e o disco persistente.
5. Depois da publicação, abra a URL HTTPS fornecida pelo Render.

Para receber fotos, vídeos e áudios com segurança em produção, é recomendado trocar o armazenamento local por S3 ou Cloud Storage.

