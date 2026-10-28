# Academia da Manicure

Projeto Vue 3 + Vite, adaptado do projeto enviado. A página principal segue a referência de link na bio: logo, dois cartões de cursos e navegação compacta.

## Executar no VSCode
1. Instale uma versão LTS do Node.js compatível com Vite 6 (Node 22 recomendado).
2. Extraia o ZIP e abra esta pasta no VSCode.
3. Abra Terminal > Novo terminal.
4. Execute `npm install`.
5. Execute `npm run dev` e abra o endereço informado no terminal.
6. Para produção: `npm run build`. A saída fica em `dist`.
7. Para conferir a compilação local: `npm run preview`.

## Onde editar
- `src/config/siteConfig.js`: cursos, agenda, WhatsApp, endereço, redes, avaliações, fotos e perguntas frequentes.
- `src/App.vue`: estrutura das páginas.
- `src/style.css`: cores, tamanhos, espaçamento e responsividade.
- `public/media`: imagens locais.
- `src/components/AccessibilityMenu.vue`: recursos preservados do projeto original, incluindo VLibras sob demanda e leitura em voz alta.

## Dados pendentes
O WhatsApp fica oculto até preencher `whatsapp` com DDI + DDD + número, apenas dígitos. O botão gera a mensagem do curso escolhido. Não há processamento de pagamento nem envio de documentos neste site.

Preencha `address` e `mapUrl`. Adicione redes em `socials: [{name: 'Instagram', url: 'https://...'}]`. Adicione fotos em `photos: [{src: '/media/foto.jpg', alt: 'Descrição da foto'}]`. Adicione avaliações autorizadas em `reviews: [{name: 'Nome', text: 'Depoimento'}]`.

A galeria abre fotos em um diálogo nativo acessível. Fotos e depoimentos aguardam envio do cliente. Endereço, mapa, WhatsApp, YouTube, Facebook e Pinterest configurados em 17/10/2026. Os botões de preço enviam o nome do curso ao WhatsApp da escola, sem exibir preços no site. As duas imagens usadas nos cartões vieram dos materiais Gamma enviados, não de fotos novas dos resultados. A logo é o arquivo fornecido pelo cliente.

Os dados dos cursos foram organizados a partir das apresentações fornecidas. Em 17/10/2026, os preços e condições de pagamento foram removidos a pedido do cliente. Os dois cartões usam verde e branco. A página inicial exibe dúvidas, depoimentos, galeria, matrícula, agenda, localização e redes sociais abertas, nesta ordem. O ano da turma de Manicure/Pedicure deve ser confirmado com a escola antes da divulgação pública.

## Rotas
Início `/`; bio `/links`; demais páginas usam hash para portabilidade: `#/curso/nail-designer`, `#/curso/manicure-pedicure`, `#/duvidas`, `#/avaliacoes`, `#/galeria`, `#/matricula`, `#/agenda`, `#/localizacao`, `#/redes`. Em hospedagem estática sem fallback, use `/#/links` como alternativa à rota `/links`.

## Publicar na Vercel
1. Crie um repositório no GitHub e envie os arquivos desta pasta (sem node_modules).
2. No painel da Vercel, importe o repositório.
3. Framework: Vite. Comando de build: `npm run build`. Pasta de saída: `dist`.
4. Publique. `vercel.json` permite acesso direto à rota `/links`.
5. Atualizações enviadas à branch conectada geram nova implantação.

## Validação
Build de produção concluído e verificação estrutural de conteúdo, rotas e arquivos locais realizada. Teste visual em navegador, Lighthouse e interação com VLibras não foram executados neste ambiente; não há pontuação de performance declarada. Faça a revisão final no celular antes de divulgar ao público.

O projeto preserva Vue e o componente de acessibilidade. Dependências, imagens e componentes jurídicos não usados foram removidos. Os recursos de serviços de salão foram adaptados para consulta de cursos e matrícula.


## Atualização visual de 23/10/2026
Página inicial com abertura inspirada na referência, sem menu superior. Dúvidas, avaliações, galeria, agenda e localização abrem por botões em páginas separadas. Redes sociais no final usam ícones coloridos de 58–60 px. Botões de e-book e matrícula mantêm o WhatsApp. A seção separada de matrícula continua removida. Navegação para dúvidas e retorno ao início foram verificados no navegador; layout desktop inspecionado.
