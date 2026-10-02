# Portfolio — Design, UX e Performance Spec

Este arquivo registra os guardrails aplicados ao portfólio para manter o projeto consistente nas próximas evoluções.

## Skills aplicadas

- UI/UX Master: hierarquia visual, design system, contraste, acessibilidade, motion e conversão.
- Mobile App UX Master: mobile-first, touch targets, navegação com uma mão e experiência responsiva real.
- Performance Optimization Master: LCP/CLS/INP, lazy loading, imagens leves, carregamento progressivo e redução de recursos externos.
- Fullstack Architecture Master: separação de responsabilidades, código sustentável e degradação graciosa.
- Advanced Technical Skills Master: confiabilidade, fallback, dependências externas controladas e manutenção futura.
- Copy Marketing Master: headline orientada a benefício, prova social, escaneabilidade e CTA claro.
- Security Protection Master: links externos com noopener/noreferrer, sem secrets no frontend e mínimo de terceiros.
- SEO Master: title/description/OG, semântica, headings e conteúdo legível por crawlers.
- High Value Skills Suite: apresentação de projetos como cases e não apenas galeria visual.
- SaaS Dashboard Master: organização por leitura rápida e redução de carga cognitiva.
- AI/Automation skills: usadas como contexto dos cases e posicionamento; o portfólio não depende de API de IA para renderizar.
- Database/Supabase skills: não adicionam banco ao portfólio estático; mantido sem backend para máxima velocidade.

## Regras de performance

1. Nenhum iframe de projeto pode existir no carregamento inicial.
2. Previews pesados devem usar IntersectionObserver e ser montados somente perto da viewport.
3. Iframes de previews reais devem ser desmontados após ficarem fora da área visível.
4. Vídeos do YouTube usam thumbnail primeiro e player somente após clique.
5. Imagens abaixo da dobra usam loading="lazy" e decoding="async".
6. Hero usa asset local otimizado e fetchpriority="high".
7. Animações devem preferir transform/opacity e respeitar prefers-reduced-motion.
8. Não adicionar bibliotecas JS grandes apenas para animação.
9. Meta: LCP < 2.5s, CLS < .1 e INP < 200ms em condições razoáveis.

## Regras de previews

- Nunca inventar uma screenshot para representar um site existente.
- GitHub Pages usa a própria página como preview real carregado sob demanda.
- Screenshots do Lovable podem ser usados quando representam fielmente o projeto.
- Se uma screenshot estiver ruim/desatualizada, usar preview real sob demanda em vez de um mock.
- O modal de projeto pode carregar o site real somente por ação explícita do visitante.

## Mobile-first

- Touch targets >= 44px para ações principais.
- Dock inferior somente no mobile para Projetos, Vídeos e WhatsApp.
- Modal de projeto ocupa a tela inteira no mobile.
- Sem hover como requisito funcional.
- Grids viram uma coluna em telas pequenas.
- Evitar animações 3D em touch devices.

## Direção visual

- Fundo quase preto: #05080d.
- Azul principal: #238cff.
- Azul claro: #63b5ff.
- Tipografia branca com cinzas azulados.
- Estética: futurista, tecnológica, premium e limpa; evitar excesso de glow e elementos decorativos sem função.
- Motion deve reforçar navegação, profundidade e sensação de produto digital.

## Posicionamento

Headline:
**Estratégia digital que gera oportunidades.**

Oferta resumida:
**Sites • Landing Pages • Tráfego Pago • Criativos • Automação • IA**

O portfólio deve posicionar Douglas Alves como profissional que conecta estratégia, marketing, produto, tecnologia e execução, não apenas como editor de vídeo.

## Checklist antes de publicar

- [ ] Nenhum preview fictício representando site real.
- [ ] Mobile 360px, 390px, 430px sem overflow horizontal.
- [ ] Desktop 1366px e 1920px visualmente equilibrado.
- [ ] CTAs visíveis e claros.
- [ ] Links externos funcionam em nova aba com proteção adequada.
- [ ] Conteúdo principal aparece mesmo se JavaScript falhar.
- [ ] prefers-reduced-motion respeitado.
- [ ] Sem secrets, tokens ou chaves no HTML.
- [ ] Previews não bloqueiam o carregamento inicial.
- [ ] GitHub Pages deploy concluído com sucesso.
