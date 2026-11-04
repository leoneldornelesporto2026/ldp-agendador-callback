# Checklist de revisão TikTok — LDP Agendador
Data: 2026-11-04

## Motivos apresentados pelo revisor
1. Ícone no TikTok, site e favicon diferentes.
2. Website URL aponta para página simples de apresentação, não para um site completo.

## Correções de site
- Site oficial: https://leoneldornelesporto2026.github.io/ldp-agendador-callback/
- Página inicial com descrição dos fluxos reais, navegação para Recursos, Guia e Suporte.
- Privacidade, Termos de Serviço e Exclusão de dados acessíveis diretamente na navegação e no rodapé.
- Favicon e logo do site derivados do ícone oficial apresentado pelo responsável.
- Página apresentacao.html preservada para compatibilidade com links antigos.
- Referências a arquivos inexistentes google/privacidade.html e google/termos.html removidas.
- Documentação TikTok ajustada para user.info.basic, video.upload, video.publish e restrições de Direct Post.

## Ações manuais necessárias no TikTok for Developers
1. Substituir App icon pelo PNG fornecido de 1024x1024 (não pelo SVG do site).
2. Alterar Web/Desktop URL para a homepage acima (não apresentacao.html).
3. Confirmar que a descrição do aplicativo e o vídeo demonstrativo correspondem à implementação efetiva.
4. Verificar na Sandbox todos os produtos e escopos solicitados.
5. Manter o callback OAuth local registrado conforme a implementação desktop; não transferir segredos para o site.
6. Reenviar a revisão somente após testar todas as URLs publicadas e a demonstração do produto.

## Atenção
Regras do TikTok não aprovam apps exclusivamente para uso privado/pessoal ou ainda em desenvolvimento/teste. Este site apresenta o serviço publicamente, mas não altera seu estado real de entrega nem garante a aprovação. Nenhum escopo, login ou capacidade de publicação foi alterado nesta correção de site.
