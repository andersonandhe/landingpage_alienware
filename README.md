# Landing page — Alienware 16 Aurora

Landing page de análise independente do notebook Alienware 16 Aurora (RTX 4050, tela 120 Hz, Wi-Fi 7), voltada para quem joga Warzone e outros FPS competitivos. Página estática em pt-BR com links de afiliado da Amazon.

## Estrutura

- `index.html` — página única, com todo o CSS e JS embutidos. Sem etapa de build.

## Seções

1. **Hero** — animação de abertura do notebook controlada por scroll (GSAP ScrollTrigger).
2. **Loadout** — os 6 componentes apresentados como slots de equipamento, com nota de 0 a 10.
3. **Especificações** — ficha técnica completa em cards.
4. **Comparativo** — "é para você se / procure outra configuração se".
5. **120 Hz** — demonstração visual de 60 Hz vs 120 Hz.
6. **Dúvidas** — FAQ em `<details>`.
7. **Chamada final** + barra fixa com CTA para a Amazon.

## Dependências (via CDN)

- [GSAP 3.12 + ScrollTrigger](https://gsap.com/) — animações de scroll. A página funciona normalmente sem elas (fallback sem animação).
- Google Fonts — Chakra Petch e Barlow.

Suporta tema claro/escuro (`prefers-color-scheme`) e `prefers-reduced-motion`.

## Como rodar

Basta abrir o `index.html` no navegador, ou servir a pasta:

```sh
python3 -m http.server 8000
```
