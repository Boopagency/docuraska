# Doçuras.Ka · link na bio

Página do link na bio da [@docuras.ka](https://www.instagram.com/docuras.ka/), doceria artesanal em São José dos Pinhais – PR.

Quem clica na bio entende o que a Ka faz e escolhe um caminho:

- **Fazer meu pedido**: formulário curto para quem já sabe o que quer (nome, WhatsApp, pedido, data e retirada ou entrega).
- **Pedir orçamento**: formulário para festa, evento ou presente (ocasião, data, convidados, o que orçar, local e detalhes).
- **Ver o cardápio**: abre direto, sem formulário.

Os dois formulários montam a mensagem e abrem a conversa no WhatsApp da Ka com tudo organizado.

## Ver no computador

```bash
python3 -m http.server 8000
```

Depois abra http://localhost:8000.

## Configuração

No começo do `<script>` do `index.html`:

| Constante | Hoje | O que é |
| --- | --- | --- |
| `PREVIA` | `false` | `true` mostra o selo "Prévia" e o envio só exibe a mensagem, sem abrir o WhatsApp |
| `WHATSAPP` | `5541992285860` | número da Ka: (41) 99228-5860 |
| `CARDAPIO_URL` | vazio | link do cardápio (PDF ou imagem). Vazio, o botão abre o WhatsApp pedindo o cardápio |
| `LEADS_URL` | vazio | opcional: para onde mandar os contatos (planilha ou Comercial do Boop Admin) |

Ainda falta:

- O arquivo do cardápio.
- Confirmar com a Ka o nome para o bloco "Quem faz" e se ela faz entrega.
- Fotos de produto em alta resolução (as da vitrine têm uns 500 px). Ao trocar uma foto, use um nome novo de arquivo (veja Desempenho).

## Arquivos

- `index.html`: a página inteira, com estilo e script.
- `assets/`: fotos, logo, abelha, favicon e a fonte Bricolage Grotesque (servida pelo próprio site).
- `vercel.json`: cache longo para `assets/`.

## Desempenho

- Imagens em WebP (o nome da marca em PNG de 16 cores), no tamanho em que aparecem.
- Fonte reduzida aos caracteres do português e sem o eixo de tamanho ótico: 57 KB.
- A foto do topo e o título aparecem na hora; o movimento fica nos detalhes e respeita quem pediu menos movimento no aparelho.
- `vercel.json` guarda `assets/` em cache por um ano. Ao trocar uma foto, salve com outro nome (ex.: `hero-2.webp`) e atualize o `index.html`; com o mesmo nome, quem já visitou continua vendo a antiga.
- Lighthouse no celular (local): desempenho 99, acessibilidade 100, boas práticas 100, SEO 100.
