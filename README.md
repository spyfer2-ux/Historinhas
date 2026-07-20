# 🌙 Historinhas

App de leitura para pais e filhos — contos clássicos com o nome do seu filho (e o seu!) dentro da história.

## ✨ Funcionalidades

- **32 histórias** em português, organizadas em 5 categorias:
  - 📖 **Contos Clássicos** (12) — domínio público: Grimm, Perrault, Andersen, Collodi, Mil e Uma Noites
  - 🕵️ **Suspense & Mistério** (5) — sustinhos do bem, sempre com final divertido (originais)
  - 🗺️ **Aventura** (5) — tesouros, selvas, mares e montanhas (originais)
  - 💙 **Turminha TEA** (5) — histórias inclusivas com protagonistas autistas, escritas com carinho: fones de ouvido, cantinho calmo, rotina visual, hiperfoco como superpoder (originais)
  - 🦸 **Heróis** (5) — capas, escudos e corações valentes (originais)
- 7 histórias grátis (1 de amostra em cada categoria nova + 3 clássicos) e 25 premium
- 🪄 **Nomes mágicos**: o nome da criança vira o herói e o nome do pai/mãe vira um personagem adulto (Gepeto, o Rei, o Gênio, o lenhador...)
- ▶️ **Leitura por IA** (voz do aparelho), com botão rápido de voz feminina 👩 e masculina 👨
- 🔄 **Autoscroll** com controle de velocidade
- 🔊 **Efeitos sonoros** automáticos durante a leitura (lobo, batida na porta, chuva, magia...) — gerados por código, sem arquivos de áudio
- 📢 Espaços de anúncio marcados (topo, meio, rodapé, leitor + intersticial e anúncio premiado)
- 💰 Compras: **Remover anúncios R$ 19,90** e **Passe Mágico (todas as histórias) R$ 14,90** — em modo demonstração

## 🚀 Como publicar (GitHub Pages) — grátis

1. Abra o repositório `spyfer2-ux/historinhas` no GitHub
2. Toque em **Add file → Upload files** e envie `index.html` e este `README.md`
3. **Commit changes**
4. Vá em **Settings → Pages**
5. Em "Source", escolha **Deploy from a branch**, branch `main`, pasta `/ (root)` e salve
6. Em ~1 minuto o app estará no ar em: `https://spyfer2-ux.github.io/historinhas/`

Abra no celular e use "Adicionar à tela inicial" — funciona como app.

## 💵 Ativando a monetização de verdade

O app está com **placeholders** nos pontos certos:

- **Banners**: troque as `<div class="ad">` pelo código do Google AdSense (versão web) ou AdMob (versão Android)
- **Intersticial/premiado**: a função `showInter()` simula o anúncio de tela cheia — substitua pela chamada do AdMob Interstitial/Rewarded
- **Compras**: procure `PAGAMENTO_AQUI` no código. Na versão web, use um gateway com Pix (Mercado Pago, por exemplo). Na versão Android (Play Store), use o Google Play Billing com dois produtos: `remover_anuncios` (R$ 19,90) e `passe_magico` (R$ 14,90)

## 📱 Virando app Android (Play Store)

O caminho mais simples: empacotar este site como **TWA** (Trusted Web Activity) com o [Bubblewrap](https://github.com/GoogleChromeLabs/bubblewrap) ou o site [PWABuilder](https://www.pwabuilder.com) — você cola a URL do GitHub Pages e ele gera o APK/AAB para enviar à Play Store.

## ⚖️ Importante — direitos autorais

Todas as histórias são **adaptações originais de contos de domínio público** (os mesmos contos que inspiraram os filmes famosos: Cinderela, Branca de Neve, A Pequena Sereia, Rapunzel, A Rainha da Neve...). **Não use nomes ou personagens da Disney/Pixar** (nem variações como "Woodie" ou "Buzzy") — isso é violação de marca/direito autoral, gera remoção do app nas lojas e risco de processo. A história "A Turma do Baú de Brinquedos" é 100% original, com personagens próprios.

## ➕ Adicionando novas histórias

No `index.html`, dentro de `const STORIES=[...]`, copie um bloco de história e edite. Tokens:

- `{H}` = nome da criança (herói)
- `{P}` = nome do pai/mãe (personagem adulto)
- `sfx` = efeito sonoro do parágrafo: `magic, wolf, knock, steps, rain, wind, splash, creak, bell, pop, fanfare, heart, night, fire, roar, bird, laugh, snore, whoosh`
