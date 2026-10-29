# L.D.Porto Agendador — Páginas públicas para Google OAuth

Páginas criadas em 29/10/2026:

- `index.html` — página inicial.
- `privacidade.html` — Política de Privacidade.
- `termos.html` — Termos de Serviço.
- `exclusao-de-dados.html` — instruções de revogação e exclusão (útil também em integrações Meta).
- `styles.css` — layout responsivo, independente de serviços externos.
- `favicon.svg` — ícone de identificação do site (não é o logotipo exigido no formulário OAuth).

## Antes de publicar — revisão obrigatória

- Confirmar com o código real quais dados do YouTube e demais plataformas são coletados e retidos.
- Confirmar como os tokens OAuth são protegidos, os prazos de retenção e o fluxo de exclusão local.
- Se o aplicativo for distribuído para outras pessoas, adaptar os textos à realidade de atendimento e operação.
- **IMPORTANTE PARA YOUTUBE:** as políticas exigem concordância com Política de Privacidade antes de usar os recursos de API, e que essa política seja visível no próprio aplicativo. Também definem atualização/exclusão de alguns dados a cada 30 dias e remoção de dados associados em até 7 dias após solicitação. Solicitar ao Sol implementar/auditar essas exigências antes de enviar o aplicativo para verificação.
- As páginas jurídicas foram redigidas para o cenário conhecido de aplicativo desktop de uso pessoal; não substituem revisão jurídica, nem a documentação técnica do código.
- As páginas são **públicas** quando publicadas. Não enviar arquivos `.env`, credenciais, SQLite, backup ou dados pessoais ao serviço de hospedagem.

## Publicação sugerida: Cloudflare Pages

1. Abra https://dash.cloudflare.com/ e vá a **Workers & Pages**.
2. Escolha criar **Pages** com **Direct Upload / Upload assets**.
3. Nomeie o projeto, por exemplo `ldp-agendador-site`, se estiver disponível.
4. Envie o ZIP de site, ou a pasta contendo `index.html` e os demais arquivos.
5. Publique e anote **o endereço exato exibido pela Cloudflare**. O endereço não existe antes do deploy e seu nome não é garantido.
6. Idealmente associe um **domínio seu** ao Pages para passar pelo processo de verificação de domínio do Google. Caso utilize apenas `pages.dev`, verifique com atenção o requisito de domínio verificável no Google; não assuma aprovação automática.
7. Acesse cada página em janela anônima para confirmar que nenhuma exige login.

## Campos Google Auth Platform → Branding

Nome: L.D.Porto Agendador
Suporte: ldornelesporto@gmail.com
Logotipo OAuth: deixar vazio inicialmente, pois upload de logotipo pode exigir revisão.
Página inicial: https://SEU-DOMINIO-VERIFICADO/ (apenas depois de publicar)
Política: https://SEU-DOMINIO-VERIFICADO/privacidade.html
Termos: https://SEU-DOMINIO-VERIFICADO/termos.html
Domínios autorizados: o domínio cujo controle você puder comprovar, sem protocolo nem barra (regra Google para domínio registrável).
Contato desenvolvedor: ldornelesporto@gmail.com

**IMPORTANTE:** os endereços `SEU-DOMINIO-VERIFICADO` são placeholders, não URLs reais. Não colar esses placeholders no console.

## Verificação de domínio

A documentação Google sobre verificação OAuth exige comprovação de domínio e associação do site/Política à marca. Para uma revisão de marca, normalmente se verifica o domínio registrável no Search Console com usuário proprietário/editor do projeto Google Cloud. Um domínio próprio com verificação DNS TXT é o caminho mais robusto.

https://console.cloud.google.com/auth/branding?project=ldp-agendador-510315
https://console.cloud.google.com/auth/audience?project=ldp-agendador-510315
https://search.google.com/search-console

## Próximo passo para corrigir invalid_grant

Quando as páginas estiverem publicadas e a plataforma Google permitir status Em produção, avaliar as exigências de verificação dos escopos YouTube. Mudar o status não revive refresh token expirado: autorizar novamente pelo Agendador após a alteração, com a mesma conta e o cliente OAuth correto. Não criar novas credenciais desnecessariamente.

Documentação:
- https://support.google.com/cloud/answer/13464321
- https://support.google.com/cloud/answer/13807376
- https://support.google.com/cloud/answer/13806988
- https://developers.google.com/identity/protocols/oauth2/
- https://developers.cloudflare.com/pages/get-started/direct-upload/
