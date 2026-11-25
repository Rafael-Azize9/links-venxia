# Venxia — Página de links

Projeto oficial da Venxia: uma página de links simples, organizada e otimizada
para celular, onde reunimos nossos canais de atendimento em um só lugar —
WhatsApp, site, e-mail e localização.

Tudo foi feito com HTML e CSS puro, sem dependências ou etapa de build. O
resultado é uma experiência leve, com visual minimalista de fintech, fundo em
gradiente azul e animações discretas.

## Sobre o projeto

- Página única (`index.html`), responsiva e com suporte a notch/`safe-area`.
- Canais centralizados em cards, com hierarquia visual clara.
- Favicon, preview para redes sociais e selo de presença "Online agora".
- Acessibilidade: foco visível, `aria` e respeito a `prefers-reduced-motion`.

## A logo da Venxia

A logo foi adicionada a partir do arquivo original fornecido
(`B4F8B9EA-499F-43D5-ABAA-E59238298C20.png`, salvo em Downloads). Como a
imagem original é vertical e o símbolo "X" ocupa pouco espaço, foi feito um
recorte quadrado centralizado no símbolo, gerando o `logo.png` usado no topo da
página dentro de um círculo com anel de gradiente animado.

A mesma marca aparece em outros pontos:

- `logo.png` — avatar/cabeçalho e ícone "apple-touch-icon".
- `favicon.svg` e `favicon.png` — ícone da aba do navegador.
- `og-image.png` — imagem de preview (1200×630) para WhatsApp e redes sociais.

## Propriedade e direitos autorais

Este é um projeto da **Venxia**. O código, o layout, os textos, a logo e os
demais arquivos deste repositório são de propriedade da Venxia e destinam-se
exclusivamente à divulgação dos seus canais oficiais de contato.

© 2026 Venxia. Todos os direitos reservados.

É permitido visualizar e compartilhar o link público da página. A reutilização,
cópia, modificação ou distribuição do conteúdo deste repositório sem
autorização expressa da Venxia não é permitida.

## Como usar

Abra o `index.html` no navegador, ou hospede a pasta inteira em qualquer
servidor estático (GitHub Pages, Netlify, Vercel, host de sua preferência).
Não precisa de instalação nem de build.

## GitHub

Repositório: https://github.com/Rafael-Azize9/links-venxia (branch `main`).

Para publicar com GitHub Pages: **Settings → Pages → Build and deployment →
Deploy from a branch → main / root**. Depois, o endereço será
`https://rafael-azize9.github.io/links-venxia/`.

Se for usar esse endereço, troque `venxia.com` pelas tags `og:url`, `og:image`
e `twitter:image` para que o preview no WhatsApp funcione.

## O que editar

Tudo fica no `index.html`. Procure pelos trechos abaixo:

Dados já configurados: **Venxia**, WhatsApp `(88) 99699-6085`, site `venxia.com`, e-mail `contato.venxia@gmail.com`, endereço `Av. da Abolição, Loja 01 – Meireles, Fortaleza/CE – CEP 60165-078`.

| O que mudar | Onde está |
|---|---|
| Nome da empresa e descrição | `<header class="perfil">` |
| Logo | Já configurada: `logo.png` (recorte da imagem original em Downloads). Para trocar, substitua o arquivo mantendo o nome ou edite o `src` do `<img class="avatar">` |
| Favicon | Embutido no `<head>` como data URI (funciona mesmo sem os arquivos externos). Arquivos: `favicon.svg` e `favicon.png` (fallback). Para trocar, edite a linha `rel="icon"` e os arquivos |
| Preview no WhatsApp | Tags Open Graph e Twitter Card no `<head>`. A imagem é `og-image.png` (1200×630). **Troque `venxia.com` pelo domínio real onde esta página estiver publicada** nas tags `og:url`, `og:image` e `twitter:image` |
| Número do WhatsApp | No link `wa.me/5588996996085` (use DDI + DDD + número, só dígitos) |
| Mensagem automática do WhatsApp | No parâmetro `?text=` (já codificado em URL) |
| Site | `href="https://venxia.com"` e o texto da descrição |
| E-mail | `href="mailto:contato.venxia@gmail.com"` e o texto da descrição |
| Endereço | `<address>` no rodapé |
| Link do mapa | `href` do "Ver no mapa" (link do Google Maps) |
| Ano/direitos | `<p class="rodape__copyright">` |
| Cores | Variáveis no bloco `:root` do CSS |

## Animações

Tudo é CSS puro (sem JavaScript):

- Entrada escalonada de logo, título, canais e rodapé (`fade + translate + blur`, com easing de mola).
- Anel de gradiente girando lentamente ao redor da logo.
- Orbs de luz flutuando no fundo e textura de granulado sutil.
- Selo "Online agora" com ponto verde pulsando suavemente.
- Ao tocar/passar mouse nos cards: elevação suave, ícone crescendo e varredura de luz.
- `prefers-reduced-motion`: todas as animações são desativadas para quem prefere menos movimento.

## Dicas

- Para testar no celular, use a ferramenta de inspecionar do navegador
  (modo responsivo) ou abra o arquivo pelo celular.
- O `viewport-fit=cover` + `env(safe-area-inset-*)` respeitam o "top"/notch
  de iPhones e outros aparelhos com recorte na tela.
- Ícones são SVG embutidos: não dependem de internet nem de bibliotecas.
- Os cards dos canais são centralizados (ícone, título e descrição alinhados ao centro), sem setas, para um visual mais limpo.
- Se o favicon não aparecer de imediato, é cache do navegador: faça uma recarga forçada (Ctrl+F5) ou abra em aba anônima.
- Para testar o preview do link, use o [Facebook Sharing Debugger](https://developers.facebook.com/tools/debug/) ou o [Twitter Card Validator](https://cards-dev.twitter.com/validator). O WhatsApp usa as mesmas tags Open Graph.
