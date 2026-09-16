# Landing page — Alienware 16 Aurora

Landing page de análise independente do notebook Alienware 16 Aurora (RTX 4050, tela 120 Hz, Wi-Fi 7), voltada para quem joga Warzone e outros FPS competitivos. Página estática em pt-BR com links de afiliado da Amazon, publicada sob a marca de análises **Mira**.

## Identidade visual

Direção inspirada na disciplina das páginas de produto da Apple, com identidade própria:

- **Paleta "prata e grafite + verde-aurora":** fundos neutros claros (`#F4F5F7` / `#FFFFFF`), grafite `#101114` apenas em painéis contidos, e um único acento funcional, o verde-aurora `#16D07E` (referência ao nome Aurora), reservado a ações e destaques.
- **Tipografia:** uma família só, Archivo variável (Google Fonts) — largura expandida para títulos, normal para corpo. Hierarquia por peso e largura, tracking negativo em display.
- **Botões:** pílula total (`border-radius: 999px`), verde com texto grafite; um único rótulo por intenção ("Ver preço" em todos os CTAs de compra).
- **Tom de voz:** frases curtas, benefício antes da especificação ("120 Hz. O dobro de fluidez.").

## Estrutura

- `index.html` — página única, com todo o CSS e JS embutidos. Sem etapa de build.

Seções: hero com painel aurora → aviso de transparência → três números → análise peça por peça (notas 0–10) → demo 60 vs 120 Hz → perfil (é/não é para você) → ficha técnica → dúvidas → chamada final. Dock fixo de compra aparece durante a leitura.

## Dependências (via CDN)

- [GSAP 3.12 + ScrollTrigger](https://gsap.com/) — animações de entrada por scroll. A página funciona normalmente sem elas (conteúdo visível em repouso).
- Google Fonts — Archivo (variável, eixo de largura).

Navegação ativa e dock usam `IntersectionObserver` (sem listeners de scroll). Suporte a `prefers-reduced-motion`.

## Pendências

- Substituir o painel aurora do hero por foto real do produto (marcado com `TODO` no HTML).

## Como rodar

Basta abrir o `index.html` no navegador, ou servir a pasta:

```sh
python3 -m http.server 8000
```
